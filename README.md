# Image slider by Marie

## HTML
The image slider including the h1 are place inside a div called 'container'. Inside the container there are two different div´s that holds the outer content(in this case the arrows) and the inner content, the images.

### The HTML should look like this: 

```html
 <div class="container">
        <h1>Image Slider</h1>
        <div class="slider-outer">
            <img src="img/arrow_left.png" class="prev" alt="Prev arrow">
            <div class="slider-inner">
                <img src="img/Img_1_jason-an-gnZ7krk_G_o-unsplash.jpg" class="active" alt="nature picture">
                <img src="img/img_2_quinton-coetzee-tvnp4r6xzvY-unsplash.jpg" alt="">
                <img src="img/img_3_alexandre-dinaut-GHxr3O6yZ1c-unsplash.jpg" alt="">
            </div>
            <img src="img/arrow_right.png" class="next" alt="Next arrow">
        </div>
    ...

```

## JavaScript

To make it possible to slide between the different images I implemented a onclick function for both of the arrow images. You can see how I made it work below. To check if the function is working before you write the if statement console.log(clicked).

```js

...

$('.next').on('click', function() {
        var currentImg = $('.active');
        var nextImg = currentImg.next();

        if (nextImg.length) {
            currentImg.removeClass('active').css('z-index', -10);
            nextImg.addClass('active').css('z-index', 10);
        }
    });
...

```
You will have to write the same function for the prev arrow, just like the one above. Remember to swich out 'next' with prev'. 
