# How-can-I-detect-which-javascript-engine
You can insert js code into Chrome or Firefox Console to detect which javascript engine used. For example Angular or React.  Also you can see if website build with Backbone, Ember, Vue, Meteor, Zepto frameworks. Or to detect if jQuery is used on frontend of website.

The list of all js libraries you can check:
* React
* Angular
* Bootstrap
* Backbone
* Ember
* Vue
* Meteor
* Zepto
* jQuery
* Node
* Mocha JS
* Nuxt JS
* Jasmine
* Gatsby JS
* Svelte JS

# How to use?
All you need is just open F12 Chrome or Firefox Console
1)And insert the code.

![Image of Console](https://i.stack.imgur.com/t9Z2E.png)

2)Hit Enter.

# The Code
	//react
	if(!!window.React ||
	   !!document.querySelector('[data-reactroot], [data-reactid]'))
	  console.log('React.js');
	//angular
	if(!!window.angular ||
	   !!document.querySelector('.ng-binding, [ng-app], [data-ng-app], [ng-controller], [data-ng-controller], [ng-repeat], [data-ng-repeat]') ||
	   !!document.querySelector('script[src*="angular.js"], script[src*="angular.min.js"]'))
	  console.log('Angular.js');
	//bootstrap
	if(!!document.querySelector('.col-md-3, .col-md-4, .col-md-6, .col-md-8, .col-sm-3, .col-sm-4, .col-sm-6, .col-sm-8, .col-xs-6, .col-xs-12') || !!document.querySelector('script[src*="bootstrap.min.js"],script[src*="bootstrap.bundle.min.js"],script[src*="bootstrap.js"]'))
		console.log('Bootstrap.js');
	if(!!window.Backbone) console.log('Backbone.js');
	if(!!window.Ember) console.log('Ember.js');
	if(!!window.Vue) console.log('Vue.js');
	if(!!window.Meteor) console.log('Meteor.js');
	if(!!window.Zepto) console.log('Zepto.js');
	if(!!window.jQuery) console.log('jQuery.js');
	if(!!window.Bootstrap) console.log('Bootstrap.js');
	if(!!window.Node) console.log('Node.js');
	if(!!document.querySelector('script[src*="mocha.js"]')) console.log('Mocha.js');
	//nuxt
	var inputs = document.querySelectorAll("link[rel=preload]");var regex = /^.+?\/_nuxt\/.+?$/; for (var i=0; i<inputs.length; i++) if (regex.test(inputs[i].href)) {  console.log('Nuxt.js');break;}
	//jasmine
	var inputs = document.querySelectorAll("script");var regex = /^.+?\/jasmine-.+?$/; for (var i=0; i<inputs.length; i++) if (regex.test(inputs[i].src)) {  console.log('Jasmine.js');break;}
	//Gatsby
	var inputs = document.querySelectorAll('meta[name="generator"]');var regex = /^Gatsby.+?$/; for (var i=0; i<inputs.length; i++) if (regex.test(inputs[i].content)) {  console.log('Gatsby.js');break;}
	//Svelte
	var inputs = document.querySelectorAll('div');var regex = /^svelte.+?$/; for (var i=0; i<inputs.length; i++) if (regex.test(inputs[i].id)) {  console.log('Svelte.js');break;}

If you want to thank you, use webmaster tools on http://wploader.com
