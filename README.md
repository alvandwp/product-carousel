# Responsive Product Slider

This is a responsive product slider built from scratch without any frameworks or libraries. This slider has a few lines of code, so it is lightweight and fast. I used a class that allows you to create as many sliders as you want on a web page. All images used are free and taken from [Unsplash](https://unsplash.com/).

## How to use it

First download this repository. Then follow the next steps.

### HTML Section

In the **index.html** file of the **root folder of the repository**, you can find, edit or add the slider HTML codes.

Just copy and paste the `div` tag with the `slider-container` class attribute value and change its `id` attribute value to your desired value.

Each `li` tag with the `slider-item` class is a single slide. You can add more slides, delete some, and edit the slide (`slide-link-url`, `slide-image-file-url`, and `image alternative text`) as you want.

#### Sample code:

```
<div class="slider-container" id="sample-slider">
  <div class="slides-wrapper">
    <div class="slides-container">
      <ul class="slider-list">
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
      </ul>
    </div>
  </div>
  <div class="slider-arrows">
    <button type="button" class="slider-arrow-prev">Prev</button>
    <button type="button" class="slider-arrow-next">Next</button>
  </div>
</div>

```

### JavaScript section

In the **assets** folder > **js** folder, the **slider.js** file is located. You can find, edit, or add the slider JavaScript codes there.

To create each new slider, add the following line of code at the bottom of the code before `}` and change the values:

```
new Slider('sample-slider', [576, 768, 992]).run();
```

Replace `sample-slider` with the `id` of your `slider-container` div tag that you entered earlier in the HTML section.

`[992 ,768 ,576]` is an array of media queries (breakpoints) where the number of slides displayed at the same time will increase. Change it if necessary.

Save the files. That's it! You've created a new slider.
