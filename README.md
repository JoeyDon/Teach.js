

Teach.js [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)]()
===================================
=
[![Dependency Status](https://img.shields.io/david/ckeditor/ckeditor5.svg)](https://david-dm.org/ckeditor/ckeditor5)

A set of ready-to-use Machine Learning extracted functions from [tensorflow.js]([https://www.tensorflow.org/js](https://www.tensorflow.org/js)). Made teaching your website to react based on trainning by Webcam be possible.

## Demo
https://teach-demo.firebaseapp.com/

## ⚠ This package does not support NPM install yet

Teach.js is not bundled yet by Webpack as in the early stage, which you can not [install from npm](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/installation.html#npm).

You will have to manually install the 3 dependencies. 
`npm install --save @tensorflow-models/knn-classifier @tensorflow-models/mobilenet @tensorflow/tfjs`

## Table of contents

* [Quick start](#quick-start)
   * [Install this library](#ckeditor-5-builds)
* [Packages](#packages)
   * [Core libraries](#core-libraries)
* [License](#license)

## Quick start

### Install this library

Teach.js assembles a set of ready-to-use Machine Learning functions. 


#### Example

Creating an model using a Teach build is very simple and can be implemented in these steps:

1. Download this Teach.js into your project and import as:
`import * from './lib/Teach'`
2. Create a new instance `var instance = new Teach('webcam',fn1,fn2)`. fn1 and fn2 are the functions will be invoked if trained pattern gets recognized. e.g. In the demo: 
```html
<script>
	var scrollSpeed = 20;
	fn1(){
		window.scrollBy(0, -this.scrollSpeed);
	},
	fn2(){
		window.scrollBy(0, this.scrollSpeed);
	}
</script>
```
3. `#console`  contains the webcam and reaction. 
```html
<div id="console" />
``` 
4. `#webcam` to record your action/gesture:
```html
<video autoplay playsinline muted id="webcam" width="280" height="150" />
```
5. Three buttons to train your model, in the demo:
```html 
<button onClick="instance.addExample(0)"> Default </button>
```
```html 
<button onClick="instance.addExample(1)"> Up </button>
```
addExample(1) will trigger fn1().
```html 
<button onClick="instance.addExample(2)"> Down </button>
```
addExample(2) will trigger fn2().



## Packages

### Core libraries

<table>
<thead>
	<tr>
		<th width="30%">Name</th>
		<th width="15%">Version</th>
		<th width="55%">Description</th>
	</tr>
</thead>
<tbody>

<tr>
	<td>
		<a href="https://github.com/tensorflow/tfjs-models/tree/master/knn-classifier"><code>@tensorflow/tfjs</code></a>
	</td>
	<td>
		<a href="https://github.com/tensorflow/tfjs"><img src="https://img.shields.io/npm/v/@tensorflow/tfjs.svg" alt="@ckeditor/ckeditor5-engine npm package badge"></a>
	</td>
	<td>
		A WebGL accelerated JavaScript library for training and deploying ML models.
	</td>
</tr>

<tr>
	<td>
		<a href="https://github.com/tensorflow/tfjs-models/tree/master/knn-classifier"><code>@tensorflow-models/knn-classifier</code></a>
	</td>
	<td>
		<a href="https://github.com/tensorflow/tfjs-models/tree/master/knn-classifier"><img src="https://img.shields.io/npm/v/@tensorflow-models/knn-classifier.svg" alt="@ckeditor/ckeditor5-engine npm package badge"></a>
	</td>
	<td>
		Creating a classifier using the K-Nearest Neighbors algorithm
	</td>
</tr>

<tr>
	<td>
		<a href="https://github.com/tensorflow/tfjs-models/tree/master/mobilenet"><code>@tensorflow-models/mobilenet</code></a>
	</td>
	<td>
		<a href="https://github.com/tensorflow/tfjs-models/tree/master/mobilenet"><img src="https://img.shields.io/npm/v/@tensorflow-models/mobilenet.svg" alt="@ckeditor/ckeditor5-engine npm package badge"></a>
	</td>
	<td>
		It can take as input any browser-based image elements and returns an array of most likely predictions and their confidences.
	</td>
</tr>

</tbody>
</table>



## License

For full details about the license, please check the `LICENSE.md` file.
