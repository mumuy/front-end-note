### 根据AMD规范写插件
```javascript
;(function () {
	'use strict';
	function pluginName(layer, options) {
		var something;
		options = options || {};
		this.layer = layer;
		this.param1 = options.param1||'';
	}
	var privateField = '';
	pluginName.prototype.fun1 = function(){
	
	}
	/**
	 * Factory method for creating a object
	 */
	pluginName.attach = function(layer, options) {
		return new pluginName(layer, options);
	};
    if (typeof define === 'function' && typeof define.amd === 'object' && define.amd) {

		// AMD. Register as an anonymous module.
		define(function() {
			return pluginName;
		});
	} else if (typeof module !== 'undefined' && module.exports) {
		module.exports = pluginName.attach;
		module.exports.pluginName = pluginName;
	} else {
		window.pluginName = pluginName;
	}
}());
```

### 根据CMD规范写插件
```javascript
;(function(factory) {
    // CMD/SeaJS
    if(typeof define === "function") {
        define(factory);
    }
    // No module loader
    else {
        factory('', window['ue'] = window['ue'] || {}, '');
    }
}(function(require, exports, module) {
	var pluginName = function(options){
        if(this.constructor !== pluginName){
            return new pluginName(options);
        }
        this.init(options);
        return this;
    };

    pluginName.prototype = {
        constructor : pluginName,
        init : function(options){

        }
    }

    if({}.toString.call(module) == '[object Object]' ){
        module.exports = pluginName;
    }else{
        exports.pluginName = pluginName;
    }
}));
```

### jQuery插件模板
```javascript
;(function ($, window, document, undefined) {
    $.fn.plugin = function(parameter) {
        parameter = parameter || {};
        var defaults = {

    	};
    	var options = $.extend({}, defaults, parameter);
        return this.each(function () {

        });
    };
})(jQuery, window, document);
```

### UMD中使用jQuery 插件
```javascript
// Uses CommonJS, AMD or browser globals to create a jQuery plugin.
(function (factory) {
    if (typeof define === 'function' && define.amd) {
        // AMD. Register as an anonymous module.
        define(['jquery'], factory);
    } else if (typeof module === 'object' && module.exports) {
        // Node/CommonJS
        module.exports = function( root, jQuery ) {
            if ( jQuery === undefined ) {
                // require('jQuery') returns a factory that requires window to
                // build a jQuery instance, we normalize how we use modules
                // that require this pattern but the window provided is a noop
                // if it's defined (how jquery works)
                if ( typeof window !== 'undefined' ) {
                    jQuery = require('jquery');
                }
                else {
                    jQuery = require('jquery')(root);
                }
            }
            factory(jQuery);
            return jQuery;
        };
    } else {
        // Browser globals
        factory(jQuery);
    }
}(function ($) {
    $.fn.jqueryPlugin = function () { return true; };
}));
```