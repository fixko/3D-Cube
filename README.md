# 3D Cube
Animated 3D CSS Cube

<div style="text-align:center; margin:10px">Watch the <a href="https://youtube.com/shorts/6M_VTFiJmI4" target="_blank">Animates 3D CSS Cube</a> Youtube Video</div>
<div><br/></div>

```
<div class="wrap">
    <div class="cube">
        <div class="front">
            <h2>Fullstack DEVs</h2>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
        </div>
        <div class="back">
            <h2>Back Side</h2>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
        </div>
        <div class="top">
            <h2>Top Side</h2>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
        </div>
        <div class="bottom">
            <h2>Bottom Side</h2>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
        </div>
        <div class="left">
            <h2>Left Side</h2>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
        </div>
        <div class="right">
            <h2>Right Side</h2>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
        </div>
    </div>
</div>

<style>
    body {
        background-color: #eee;
        margin: 0px;
    }

    .wrap {
        margin-top: 300px;
        perspective: 1000px;
        perspective-origin: 50% 50%;
        border-top: solid 3px #999;
        border-bottom: solid 3px #999;

        background-image: linear-gradient(135deg, #ccc 25%, #ddd 25%,
        #ddd 50%, #ccc 50%, #ccc 75%, #ddd 75%, #ddd 100%);
        background-size: 80px 80px;
        animation: bganim 3s linear 2s infinite;
    }

    @keyframes bganim {
        from { background-position: 0px; }
        to   { background-position: 80px; }
    }

    .cube {
        margin: auto;
        position: relative;
        height: 200px;
        width: 200px;
        transform-style: preserve-3d;
    }

    .cube div {
        position: absolute;
        padding: 10px;
        box-sizing: border-box;
        height: 100%;
        width: 100%;
        opacity: 0.9;
        background-color: #000;
        border: solid 1px #eee;
        color: #fff;
        font: 12px verdana;
        text-align: center;
        transition: transform 0.2s ease-in;
    }

    .cube div:hover {
        background-color: red;
    }

    .front {
        transform: translateZ(100px);
    }
    .back {
        transform: translateZ(-100px) rotateY(180deg);
    }
    .right {
        transform: rotateY(-270deg) translateX(100px);
        transform-origin: top right;
    }
    .left {
        transform: rotateY(270deg) translateX(-100px);
        transform-origin: center left;
    }
    .top {
        transform: rotateX(-270deg) translateY(-100px);
        transform-origin: top center;
    }
    .bottom {
        transform: rotateX(270deg) translateY(100px);
        transform-origin: bottom center;
    }

    .cube {
        animation: rotate 20s infinite linear;
    }

    @keyframes rotate {
        from {
            transform: rotateX(0deg) rotateY(0deg);
        }
        to {
            transform: rotateX(360deg) rotateY(360deg);
        }
    }

    .wrap:hover .front {
        transform: translateZ(200px);
    }
    .wrap:hover .back {
        transform: translateZ(-200px) rotateY(180deg);
    }
    .wrap:hover .right {
        transform: rotateY(-270deg) translateZ(100px)
        translateX(100px);
    }
    .wrap:hover .left {
        transform: rotateY(270deg) translateZ(100px)
        translateX(-100px);
    }
    .wrap:hover .top {
        transform: rotateX(-270deg) translateZ(100px)
        translateY(-100px);
    }
    .wrap:hover .bottom {
        transform: rotateX(270deg) translateZ(100px)
        translateY(100px);
    }

</style>
```
