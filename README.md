# 视频播放器

## HTML
```
<div class="video-player" id="video_wrap" style="width: auto;max-width:800px;margin:0 auto;">
    <div class="video-wrap">
        <video id="video" width="100%" preload="auto" poster="" src=""
               webkit-playsinline="true"
               x-webkit-airplay="true"
               x5-video-player-type="h5"
               playsinline>
        </video>
    </div>
    <div class="player-tips">
        <div class="playing"></div>
        <div class="waiting"><img src="img/waiting.png" alt=""></div>
        <div class="warning"></div>
        <div class="replaying"></div>
    </div>
    <div class="player-controls">
        <div class="controls-left">
            <div class="switch play">
                <svg class="icon-play" viewBox="0 0 36 36">
                    <path d="M25.8 18c0 .6-.3 1.1-.8 1.3L12.5 27c-.2.1-.5.2-.8.2-.8 0-1.5-.6-1.5-1.5V10c0-.8.7-1.5 1.5-1.5.3 0 .5.1.8.2l12.7 7.9c.4.5.6.9.6 1.4z"></path>
                </svg>
                <svg class="icon-pause" viewBox="0 0 36 36">
                    <path d="M12 9h1c.6 0 1 .4 1 1v16c0 .6-.4 1-1 1h-1c-.6 0-1-.4-1-1V10c0-.6.4-1 1-1zm11 0h1c.6 0 1 .4 1 1v16c0 .6-.4 1-1 1h-1c-.6 0-1-.4-1-1V10c0-.6.4-1 1-1z"></path>
                </svg>
                <svg class="icon-stop" viewBox="0 0 36 36">
                    <path d="M24 26H12c-1.1 0-2-0.9-2-2V12c0-1.1 0.9-2 2-2h12c1.1 0 2 0.9 2 2v12C26 25.1 25.1 26 24 26z"></path>
                </svg>
                <svg class="icon-replay" viewBox="0 0 36 36">
                    <path d="M17.9 28c-4.9 0-9-3.6-9.8-8.3V19.4c0-.8.7-1.4 1.5-1.4s1.5.6 1.5 1.4c.8 3.8 4.5 6.2 8.3 5.4s6.2-4.5 5.4-8.3c-.7-3.2-3.5-5.6-6.9-5.6-1.8 0-3.6.7-4.8 2h1.3c.8 0 1.5.7 1.5 1.5s-.6 1.6-1.5 1.6h-4c-.8 0-1.5-.7-1.5-1.5v-4c0-.8.7-1.5 1.5-1.5.7 0 1.2.5 1.4 1.1C13.6 8.7 15.7 8 17.9 8c5.5 0 10 4.5 10 10s-4.4 10-10 10z"></path>
                </svg>
            </div>
            <div class="time-current">00:00</div>
        </div>
        <div class="process-bar">
            <div class="process-bg"></div>
            <div class="process-buffer"></div>
            <div class="process-line"></div>
        </div>
        <div class="controls-right">
            <div class="time-duration">00:00</div>
            <div class="mute-btn mute-off">
                <svg class="icon-music-off" viewBox="-2 -2 25 25">
                    <path d="M16.714 15.593l-.01-.01a1 1 0 0 1-1.705-.708c0-.287.124-.542.317-.724C16.354 13.073 17 11.614 17 10s-.645-3.072-1.682-4.151A.993.993 0 0 1 15 5.125a1 1 0 0 1 1-1c.3 0 .561.139.744.348l.017-.016A7.969 7.969 0 0 1 19 10c0 2.178-.874 4.15-2.286 5.593zm-3.999 3.122a.956.956 0 0 1-.688.28c-.009 0-.018.005-.027.005a.984.984 0 0 1-.75-.357L5.818 15H2a1 1 0 0 1-1-1V6a1 1 0 0 1 1-1h3.818l5.432-3.643A.984.984 0 0 1 12 1c.009 0 .017.005.026.005a.954.954 0 0 1 .968.967c.001.01.006.018.006.028v16c0 .009-.005.017-.005.026a.959.959 0 0 1-.28.689zM6.75 6.643A.984.984 0 0 1 6 7H3v6h3c.304 0 .567.143.75.357l4.25 2.85V3.792L6.75 6.643z"></path>
                </svg>
                <svg class="icon-music-on" viewBox="-2 -2 25 25">
                    <path fill="white"
                          d="M16.394 12.566A5.88 5.88 0 0 0 17 10a5.97 5.97 0 0 0-1.682-4.151.993.993 0 0 1-.318-.724 1 1 0 0 1 1-1c.3 0 .561.139.745.348l.016-.016A7.969 7.969 0 0 1 19 10a7.934 7.934 0 0 1-1.116 4.055l-1.49-1.489zM11 3.792L8.978 5.149 7.62 3.792l3.63-2.435A.984.984 0 0 1 12 1c.009 0 .017.005.026.005a.954.954 0 0 1 .968.967c.001.01.006.018.006.028v7.171l-2-2V3.792zm7.864 14.072a.999.999 0 0 1-1.414 0L2.136 2.55a1 1 0 1 1 1.415-1.415L18.864 16.45a1 1 0 0 1 0 1.414zM3.171 5l2 2H3v6h3c.304 0 .567.143.75.357l4.25 2.85v-3.379l2 2V18c0 .009-.005.017-.005.027a.955.955 0 0 1-.967.968c-.01 0-.019.005-.028.005a.984.984 0 0 1-.75-.357L5.818 15H2a1 1 0 0 1-1-1V6a1 1 0 0 1 1-1h1.171z"></path>
                </svg>
            </div>
            <div class="fullscreen-btn fullscreen-on">
                <svg class="icon-fullscreen-on" version="1.1" viewBox="0 0 25 25">
                    <path d="M19.7 19.7c-.2.2-.5.3-.7.3h-4c-.6 0-1-.4-1-1s.4-1 1-1h1.6l-3.3-3.3c-.4-.4-.3-1.1.1-1.4.4-.4 1-.4 1.4 0l3.3 3.3V15c0-.6.4-1 1-1s1 .4 1 1v4c-.1.2-.2.5-.4.7zM19 10c-.6 0-1-.4-1-1V7.4l-3.3 3.3c-.4.4-1 .4-1.4 0-.4-.4-.4-1 0-1.4L16.6 6H15c-.6 0-1-.4-1-1s.4-1 1-1h4c.3 0 .5.1.7.3.2.2.3.5.3.7v4c0 .6-.4 1-1 1zM7.4 18H9c.6 0 1 .4 1 1s-.4 1-1 1H5c-.3 0-.5-.1-.7-.3-.2-.2-.3-.5-.3-.7v-4c0-.6.4-1 1-1s1 .4 1 1v1.6l3.3-3.3c.4-.4 1.1-.3 1.4.1.4.4.4 1 0 1.4L7.4 18zm1.9-7.3L6 7.4V9c0 .6-.4 1-1 1s-1-.4-1-1V5c0-.3.1-.5.3-.7.2-.2.5-.3.7-.3h4c.6 0 1 .4 1 1s-.4 1-1 1H7.4l3.3 3.3c.4.4.4 1 0 1.4-.4.4-1 .4-1.4 0z"></path>
                </svg>
                <svg class="icon-fullscreen-off" version="1.1" viewBox="0 0 25 25">
                    <path fill="white" d="M16.4 9H18c.6 0 1 .4 1 1s-.4 1-1 1h-4c-.3 0-.5-.1-.7-.3-.2-.2-.3-.5-.3-.7V6c0-.6.4-1 1-1s1 .4 1 1v1.6l3.3-3.3c.4-.4 1.1-.3 1.4.1.4.4.4 1 0 1.4L16.4 9zM10 19c-.6 0-1-.4-1-1v-1.6l-3.3 3.3c-.4.4-1 .4-1.4 0-.4-.4-.4-1 0-1.4L7.6 15H6c-.6 0-1-.4-1-1s.4-1 1-1h4c.3 0 .5.1.7.3.2.2.3.5.3.7v4c0 .5-.4 1-1 1zm0-8H6c-.6 0-1-.4-1-1s.4-1 1-1h1.6L4.3 5.7c-.4-.4-.4-1 .1-1.4.4-.4 1-.4 1.4 0L9 7.6V6c0-.6.4-1 1-1s1 .4 1 1v4c0 .3-.1.5-.3.7-.2.2-.5.3-.7.3zm4 2h4c.6 0 1 .4 1 1s-.4 1-1 1h-1.6l3.3 3.3c.4.4.4 1 0 1.4s-1 .4-1.4 0L15 16.4V18c0 .6-.4 1-1 1s-1-.4-1-1v-4c0-.3.1-.5.3-.7.2-.2.5-.3.7-.3z"></path>
                </svg>
            </div>
        </div>
    </div>
</div>
```

## CSS

``` css
<link rel="stylesheet" href="vp.css">
```

## JS

```js
/**
* @options
* @param {String} el - 视频元素id
* @param {String} url - 视频地址
* @param {Number} volume - 音量
* @param {Boolean} autoplay - 是否自动播放视频
* @param {Boolean} loop - 是否循环播放视频
* @param {Boolean} mute - 是否静音播放视频
*/
var options = {
	el: "#video_wrap",
	url: 'movie.mp4',////videos.akqa.com/work/nike/nba-connected-jersey/film.mp4
	autoplay: true,
	loop: false,
	volume: 1
}
var vp=new VideoPlayer(options);
```
