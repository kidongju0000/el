<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Full Screen Image</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background-color: #f5f5f5;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .top-link {
            display: block;
            padding: 12px 20px;
            background-color: #4CAF50;
            color: white;
            text-decoration: none;
            text-align: center;
            font-weight: bold;
            border-radius: 5px;
            margin: 20px 0;
            width: 90%;
            max-width: 500px;
            z-index: 10;
        }
        
        /* 1:1 비율 이미지 컨테이너 */
        .image-container {
            width: 100vw;
            height: 100vw; /* 너비와 동일한 높이로 1:1 비율 강제 */
            max-width: 100vh; /* 세로 모드에서도 정사각형 유지 */
            max-height: 100vh;
            margin: 0 auto;
            overflow: hidden;
            position: relative;
            background: #000;
        }
        
        /* 화면을 채우는 이미지 */
        .fullscreen-image {
            width: 100%;
            height: 100%;
            object-fit: cover; /* 비율 유지하며 채움 */
            position: absolute;
            top: 0;
            left: 0;
        }
        
        /* 데스크톱 대응 */
        @media (min-width: 768px) {
            .image-container {
                width: 80vh;
                height: 80vh;
                max-width: 80vw;
                max-height: 80vw;
            }
        }
    </style>
</head>
<body>
    <a href="https://kidongju0000.github.io/home-page/" class="top-link" target="_blank">홈</a>
    
    <div class="image-container">
        <img src="https://ifh.cc/g/oKyFGB.jpg" class="fullscreen-image" alt="풀스크린 이미지">
    </div>
</body>
</html>
