# Nutshell

<a href="http://gruntjs.com/" title="Built with Grunt"><img src="https://cdn.gruntjs.com/builtwith.png" alt="Built with Grunt" align="right"></a>

**In a nutshell, simple jQuery-powered tabs.**

---

## Usage

Put [jQuery](http://jquery.com/) on your page:

```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
```

… and link to the plugin:

```html
<script src="jquery.nutshell.min.js"></script>
```

Next, Nutshell can be instantiated like so:

```html
<script>
	
	$(document).ready(function() {
		
		$('.nutshell').nutshell();
		
	});
	
</script>
```

Here's an example with all the options:

```html
<script>
	
	$(document).ready(function() {
		
		var console = (window.console || { log : function() {} });
		
		$('.nutshell').nutshell({
			
			classSelected : 'nutshell-selected',
			animIn        : { opacity: 'show' },
			animOut       : { opacity: 'hide' },
			easeIn        : 'swing',
			easeOut       : 'swing',
			speedIn       : 'fast',
			speedOut      : 'fast',
			onInit        : function() { console.log('onInit', this) },
			onAfterInit   : function() { console.log('onAfterInit', this) },
			onBeforeShow  : function($active, $inactive, $panel) { console.log('onBeforeShow', this, $active, $inactive, $panel) },
			onShow        : function($active, $inactive, $panel) { console.log('onShow', this, $active, $inactive, $panel) },
			onBeforeHide  : function($active, $inactive, $panel) { console.log('onBeforeHide', this, $active, $inactive, $panel) },
			onHide        : function($active, $inactive, $panel) { console.log('onHide', this, $active, $inactive, $panel) }
			
		});
		
		//$('.nutshell').nutshell('destroy');
		
	});
	
</script>
```

… where:

Option | Description | Default
:-- | :-- | :--
`classSelected` | Selected tab CSS class. | `nutshell-selected`
`animIn` |  What animation object to use to show the panels. | `{ opacity: 'show' }`
`animOut` | IBID, but for hiding. | `{ opacity: 'hide' }`
`easeIn` | Easing function in. | `'swing'`
`easeOut` | Easing function out. | `'swing'`
`speedIn` | Animation speed in. | `'normal'`
`speedOut` | Animation speed out. | `'normal'`
`onInit` | Callback on plugin initialization. | `$.noop`
`onAfterInit` | Callback after plugin initialization. | `$.noop`
`onBeforeShow` | Before reveal animation begins. | `$.noop`
`onShow` | After reveal animation ends. | `$.noop`
`onBeforeHide` | Before hide animation begins. | `$.noop`
`onHide` | After hide animation ends. | `$.noop`

## Demo

[![qr code](http://chart.apis.google.com/chart?cht=qr&chl=https://github.com/mhulse/jquery-nutshell/&chs=240x240)](http://mhulse.github.com/jquery-nutshell/demo/)

**Source:** [jquery.nutshell.js](https://raw.github.com/mhulse/jquery-nutshell/gh-pages/nutshell/jquery.nutshell.js) | [jquery.nutshell.min.js](https://raw.github.com/mhulse/jquery-nutshell/gh-pages/nutshell/jquery.nutshell.min.js)

---

#### LEGAL

Copyright &copy; 2013 [Micky Hulse](http://mky.io)

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this work except in compliance with the License. You may obtain a copy of the License in the LICENSE file, or at:

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

<img width="20" height="20" align="absmiddle" src="https://github.global.ssl.fastly.net/images/icons/emoji/octocat.png" alt=":octocat:" title=":octocat:" class="emoji">
