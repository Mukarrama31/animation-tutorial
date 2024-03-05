### Animation Using Css
To create an animation we first need an element to animate which I have in my HTML file.
To animate this we head over to css and add a keyframe. The systax for this is 

    ```Css
        @keyframe <name of the animation> {
             from {

            }
            to {

            }
        }
    ```

### Utility Class
Now you add utiliity class specifying different property of animation. Such as animate fast, 
animate slow, animate delay etc. You can play around with different properties. For my demo 
I added 5 utility class 

    ```Css
        .animate {
                animation-duration: 1s;
                animation-fill-mode: both;
            }
            .animate.animate--infinite {
                animation-iteration-count: infinite;
            }

            .animate.animate--delay-1s {
                animation-delay: 1s;
            }

            .animate.animate--fast {
                animation-duration: 0.6s;
            }

            .animate.animate--slow {
                animation-duration: 3s;
            }
     ```

I prepaned the animate class in each of the four utility class. It only allows the utility classes to work if the animate class in available in the same element. It helps to avoid any mistake. You can use one or more of this utility class in your HTML file to check how it works. 

### Different Type of animation 
In my demo i used 3 types of animation. Slide from left, right and rotate from center.
Slide from left:

    ```Css
        @keyframes slideInLeft{
            from {
                transform: translateX(-300px);
            }
            to {
                transform: translateX(0);
            }
        }

        .slideInLeft {
            animation-name: slideInLeft;
            animation-timing-function: ease-in;
        }
    ```
For slide in right you simply change the - value of from to + and it will slide from right. 

Another type that you can learn is rotate 
```Css
    @keyframes rotate {
        from {
            transform: rotate(0);
        }

        to {
            transform: rotate(360deg);
        }
    }
    .rotate {
        animation-name: rotate;
        animation-timing-function: linear;
    }
```
You can set the rotating degree according to your need.

There are more options for animation like bounce, side rotate.



