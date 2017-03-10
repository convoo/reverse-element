# Reverse-Element

<p align="center">
  <img alt="reverse-element" src="ReverseElement.png" width="200">
</p>

<p align="center">
Reverses children elements based on property - helpful for accessibility
</p>

<p align="center">
  <a href="https://beta.webcomponents.org/element/convoo/reverse-element"><img src="https://img.shields.io/badge/webcomponents.org-published-blue.svg"></a>
  <a href="https://gitter.im/convoo/General"><img src="https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg"></a>
  <a href="http://waffle.io/convoo/roadmap"><img src="https://badge.waffle.io/convoo/reverse-element.svg?label=In%20Progress&title=In%20Progress"></a>
</p>

---

## Install

```
bower install convoo/reverse-element --save
```

## \<reverse-element\>

Easily reverse the order of children elements in the dom while maintaining grandchildren order. With inputs and other elements that you use `tabindex` with, you need to change the dom order to reverse the tab order and not just change the visual order using CSS.

```html
<link rel="import" href="../../reverse-element/reverse-element.html">
```

### Toggleable Reverse Element
<!--
```
<custom-element-demo>
    <template>
        <link rel="import" href="../paper-toggle-button/paper-toggle-button.html">
        <link rel="import" href="../paper-input/paper-input.html">
        <link rel="import" href="reverse-element.html">
        <div>
            <template is="dom-bind">
                <next-code-block></next-code-block>
            </template>
        </div>Ï
    </template>
</custom-element-demo>
```
-->
```html
<paper-toggle-button checked="{{reverse}}"> Toggle Reverse</paper-toggle-button>

<reverse-element reverse="{{reverse}}">
<div>
    <h3>First</h3>
    <paper-input label="First"></paper-input>
</div>
<div>
    <h3>Second</h3>
    <paper-input label="Second"></paper-input>
</div>
<div>
    <h3>
        Third
    </h3>
    <paper-input label="Third Part 1"></paper-input>
    <paper-input label="Third Part 2"></paper-input>
    <paper-input label="Third Part 3"></paper-input>
</div>
</reverse-element>
```

### Reversed

<!--
```
<custom-element-demo>
    <template>
        <link rel="import" href="../paper-input/paper-input.html">
        <link rel="import" href="reverse-element.html">
        <div>
            <template is="dom-bind">
                <next-code-block></next-code-block>
            </template>
        </div>Ï
    </template>
</custom-element-demo>
```
-->
```html
<reverse-element reverse>
<div>
    <h3>First</h3>
    <paper-input label="First"></paper-input>
</div>
<div>
    <h3>Second</h3>
    <paper-input label="Second"></paper-input>
</div>
<div>
    <h3>
        Third
    </h3>
    <paper-input label="Third Part 1"></paper-input>
    <paper-input label="Third Part 2"></paper-input>
    <paper-input label="Third Part 3"></paper-input>
</div>
<div>
    <h3>Fourth</h3>
    <paper-input label="Fourth"></paper-input>
</div>
</reverse-element>
```

## Contributing

### Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### Viewing Your Application

```
$ polymer serve
```

### Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

### Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
