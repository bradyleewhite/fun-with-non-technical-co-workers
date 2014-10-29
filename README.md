fun-with-non-technical-co-workers
=================================

Because its fun to mess with co-workers



```
    (function(){
        function rotate(degrees)
        {
            $('html').css({
                '-webkit-transform':'rotate(-' + degrees + 'deg)',
                '-moz-transform':'rotate(-' + degrees + 'deg)',
                '-ms-transform':'rotate(-' + degrees + 'deg)',
                '-o-transform':'rotate(-' + degrees + 'deg)',
                'transform':'rotate(-' + degrees + 'deg)',
                '-webkit-transition':transition,
                '-moz-transition':transition,
                '-ms-transition':transition,
                '-o-transition':transition,
                'transition':transition,
                '-webkit-transform-origin':'50% 50%',
                '-moz-transform-origin':'50% 50%',
                '-ms-transform-origin':'50% 50%',
                '-o-transform-origin':'50% 50%',
                'transform-origin':'50% 50%',
                '-webkit-backface-visibility':'hidden'
            });
        }
        var degrees = 360,
            interim,
            transition = '0.8s',// how fast we flip
            interval = 10000;   // wait 10 sec before flipping
        document.onmousemove = function()
        {
            if(degrees == 0){
                rotate(0);
                degrees = 360;
            }
            clearInterval(interim);
            interim = setInterval(function(){
                rotate(degrees);
                degrees = (degrees === 360) ? 0 : degrees;
            },interval);
        }
    })();
```
