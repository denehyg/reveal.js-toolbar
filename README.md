# reveal.js-toolbar

A toolbar plugin for [Reveal.js](https://github.com/hakimel/reveal.js) to quickly access Reveal functionality.

This plugin is compatible with the [reveal.js-menu](https://github.com/denehyg/reveal.js-menu) plugin.

## Installation

### Bower

Download and install the package in your project:

```bower install reveal.js-toolbar```

Add the plugin to the dependencies in your presentation, as below. 

```javascript
Reveal.initialize({
	// ...
	
	dependencies: [
		// ... 
	  
		{ src: 'bower_components/reveal.js-toolbar/toolbar.js' }
	]
});
```

### npm

Download and install the package in your project:

```npm install --save reveal.js-toolbar```

Add the plugin to the dependencies in your presentation, as below. 

```javascript
Reveal.initialize({
	// ...
	
	dependencies: [
		// ... 
	  
		{ src: 'node_modules/reveal.js-toolbar/toolbar.js' }
	]
});
```

### Manual

Copy this repository into the plugins folder of your reveal.js presentation, ie ```plugins/toolbar```.

Add the plugin to the dependencies in your presentation, as below. 

```javascript
Reveal.initialize({
	// ...
	
	dependencies: [
		// ... 
	  
		{ src: 'plugin/toolbar/toolbar.js' }
	]
});
```

## Configuration

You can configure the toobar for your presentation by providing a ```toolbar``` option in the reveal.js initialization options. Note that all config values are optional and will default as specified below.

```javascript
Reveal.initialize({
	// ...

	toolbar: {
		// Specifies where the toolbar will be shown: 'top' or 'bottom'
		position: 'bottom',

		// Add button to toggle fullscreen mode for the presentation
		fullscreen: false,

		// Add button to toggle the overview mode on and off
		overview: false,

		// Add button to pause (hide) the presentation display
		pause: false,

		// Add button to show the help overlay
		help: false,

		// If true, the menu will be moved into the toolbar.
		// This requires the reveal.js-menu plugin.
		captureMenu: false,

		// If true, the playback control will be moved into the toolbar.
		// This is only relevant if the presentation is configured to autoSlide
		capturePlaybackControl: false,

		// By default the menu will load it's own font-awesome library
		// icons. If your presentation needs to load a different
		// font-awesome library the 'loadIcons' option can be set to false
		// and the menu will not attempt to load the font-awesome library.
		loadIcons: true
	},

});
```

## Ready Event

A 'toolbar-ready' event is fired when reveal.js-toolbar has loaded all non-async dependencies and is ready to start.

```javascript
Reveal.addEventListener( 'toolbar-ready', function( event ) {
	// your code
} );
```

 
## License

MIT licensed

Copyright (C) 2015 Greg Denehy
