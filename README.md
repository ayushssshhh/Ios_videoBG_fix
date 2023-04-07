# Ios_videoBG_fix

since ios doesnt allow to autoplay video without leting user to interact, so we can create a canvas to and place our desire video background. (it is an old methdo).

there's also an alternate way to autoplay video in ios by adding an event on load and with callback function which select our video tag, then  implement .play().
however, the problem i faced with this solution was that on ios device when we implement .play() through any event our video start playing in fullscreen which is not we want to happen since our video should be played in background.
using canvas was the only effective solution i can come with it.


(ps: for normal video background you can use alternative method using Jquery it work properly).
<('body').on('click touchstart', function () {
        const videoElement = document.getElementById('home_video');
        if (videoElement.playing) {
            // video is already playing so do nothing
        }
        else {
            // video is not playing
            // so play video now
            videoElement.play();
        }
});
