# Customizable scroll plugin

Small JavaScript plugin that can help you scroll through the page. You can use it as a `back to top` functionality, `go to item` functionality or to scroll inside a scrollable container.

[LIVE DEMO](https://mariuslazar93.github.io/plugins/custom-scroll/) 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* jQuery > 1.4.3

### Usage

1. Add jQuery to your page/project.

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.0.0/jquery.min.js"></script>
```

2. Add the "_custom-scroll.js" file to the page/project.

```
<script src="js/_custom-scroll.js"></script>
```

3. Initialize the plugin.

```javascript
ScrollComponent.init();
```

4. Declare the HTML structure based on your desired functionality. You can choose from these:

	4.1. **Back to top of the page**

    You have to declare an element with the `.js-scroll` class and to specify the `data-scroll-target` attribute to be equal to window.

    ```html
    <a href="#" class="js-scroll" data-scroll-target="window">back to page top</a>
    ```

    4.2. **Back to top of a scrollable container**

    You have to declare an element with the `.js-scroll` class and to specify both `data-scroll-target` and `data-scroll-container` attributes to be equal to the same section selector.

    ```html
    <section id="#section">
        ....
        <a href="#" class="js-scroll" data-scroll-target="#section" data-scroll-container="#section">back to section top</a>
    </section>
    ```

    4.3. **Go to item**

    You have to declare an element with the `.js-scroll` class and to specify the `data-scroll-target` attribute to be equal to the selector of the item.

    ```html
    <a href="#" class="js-scroll" data-scroll-target="#item">go to item</a>
    ...
    <div id="item"></div>
    ```

    4.4. **Go to item inside a scrollable container**

    You have to declare an element with the `.js-scroll` class and to specify the `data-scroll-target` attribute to be equal to the selector of the item and also, you have to specify the `data-scroll-container` to be equal to the selector of the container.

    ```html
    <section id="#section">
        ....
        <div id="item"></div>
        ...
        <a href="#" class="js-scroll" data-scroll-target="#item" data-scroll-container="#section">go to item</a>
        ...
    </section>
    ```

## Configuration

### Default configuration

```javascript
var defaults = {
        sourceElement: '.js-scroll',
        duration: 400
    };
```

### Changing defaults

You can change the default configuration by initializing the plugin with other values.

```javascript
ScrollComponent.init({
        sourceElement: '.scroll',
        duration: 800
    })
```


## Example

Clone or download this repo locally and open index.html inside a browser.

**_Please use a modern browser because the current example uses flexbox for the minimal page styling._**

## Next steps

* Adding others options like easing functions
* Complete replace of jQuery with vanilla JavaScript

## Authors

* **Marius Lazar**

## License

This project is licensed under the MIT License
