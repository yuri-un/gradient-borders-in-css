# Gradient Borders in CSS
 
CSS borders in general and gradient CSS borders particularly is a powerfull tool to build fast, effective, cool graphical effect solutions. There are different methods and hooks to do this...

## Using Border Image

* Pros: easy to implement and configure.

* Cons: rounded corners aren't supported, clipped corner colors, all border sides sholud have identical parameters.

HTML:
```html
        <div class="sample-1">
            <h2>Using Border Image</h2>
            <p><b>Pros:</b> easy to implement and configure.</p>
            <p><b>Cons:</b> rounded corners aren't supported, clipped corner colors, all border sides should have identical parameters.</p>
        </div>
```

CSS:
```css
.sample-1{
    border: 10px solid red;
    border-image:linear-gradient(45deg, red, blue);
    border-image-slice:4;
    border-image-repeat:repeat;
    border-radius:5px;
}
```

## Using Background Image

* Pros: Easy to implement and configure, allows rounded corners, no clipping corner colors.

* Cons: all border sides sholud have identical parameters, inner border radius isn't allowed.

HTML:
```html
        <div class="sample-2">
            <h2>Using Background Image</h2>
            <p><b>Pros:</b> Easy to implement and configure, allows rounded corners, no clipping corner colors.</p>
            <p><b>Cons:</b> all border sides should have identical parameters, inner border radius isn't allowed.</p>
        </div>
```

CSS:
```css
.sample-2{
    border: 10px double transparent;
    background-image:linear-gradient(white, white), linear-gradient(45deg, red, blue);
    background-origin:border-box;
    background-clip:padding-box, border-box;
}
```

## Using Nested Divs

* Pros: allows to create any type of borders, inner and outer border radius is well configurable, border area can be easily filled with any html elements.

* Cons: is more complex to implement, requires at least two nested divs (more resources), it's not a direct CSS border manipulation.

HTML:
```html
        <div class="sample-3">
            <ul class="menu">
                <li><i class="fa fa-bars"></i></li>
                <li><i class="fa fa-file"></i></li>
                <li><i class="fa fa-cloud"></i></li>
                <li class="menu-button"><i class="fa fa-cog"></i></li>
            </ul>
            <div class="inner-section">
                <h2>Using Nested Divs</h2>
                <p><b>Pros</b>: allows to create any type of borders, inner and outer border radius is well configurable, border area can be easily filled with any html elements.</p>
                <p><b>Cons</b>: is more complex to implement, requires at least two nested divs (more resources), it's not a direct CSS border manipulation.</p>
            </div>
        </div>
```

CSS:
```css
.sample-3{
    padding:40px 10px 10px 10px;
    background-image:linear-gradient(45deg, red, blue);
    border:1px solid #888;
    border-radius:10px;
}

.sample-3 > .inner-section{
    padding:2em;
    background-color:#fff;
    border:0px 1px 1px 1px solid #ccc;
    border-radius:0px 0px 5px 5px;
}
```
