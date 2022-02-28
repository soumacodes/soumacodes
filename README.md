- <!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>animations with circles</title>
   <style>*{
    padding: 0%;
    margin: 0%;
    box-sizing: border-box;
}
body{
    display: flex;
    align-items: center;
    justify-content: center;
    /* width: 100%; */
    min-height: 100vh;
    background-color: black;
}
.container{
    position: relative;
    width: 250px;
    height: 250px;
    border-radius: 50%;
    overflow: hidden;
    transform: rotate(175deg);

}
    .container span{
        position: absolute;
        top: calc(12px * var(--i));
        bottom: calc(12px * var(--i));
        right:calc(12px * var(--i));
        left:calc(12px * var(--i));
        border: 10px solid black;
        border-top: 10px solid rgb(11, 247, 11);
        border-left:10px solid rgb(11, 247, 11) ;
        border-radius: 50%;
        animation: ani 1s alternate ease-in-out infinite;
        filter: hue-rotate(calc(60deg * var(--i)));
        animation-delay: calc(0.1s* var(--i));
    }
    @keyframes ani{
        0%{
            transform: rotate(0deg);
        }
        100%{
            transform: rotate(90deg);
        }
    }</style>
</head>

<body>
    <div class="container">
        <span style="--i:0;"></span>
        <span style="--i:1;"></span>
        <span style="--i:2;"></span>
        <span style="--i:3;"></span>
        <span style="--i:4;"></span>
        <span style="--i:5;"></span>
        <span style="--i:6;"></span>
        <span style="--i:7;"></span>
        <span style="--i:8;"></span>
        <span style="--i:9;"></span>
    </div>
</body>

</html>
