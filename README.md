<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>热门活动</title>
    <link rel="stylesheet" href="css/font.css">
    <link rel="stylesheet" href="css/style.css">
    <style>
        /*视频部分 */
        .video-section {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin: 40px auto;
            max-width: 1200px;
        }
        
        .video-container {
            width: 48%;
            margin-bottom: 30px;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .video-container h2 {
            padding: 15px;
            color: #FF0036;
            text-align: center;
            border-bottom: 1px solid #eee;
        }
        
        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 比例 */
            height: 0;
            overflow: hidden;
        }
        
        .video-wrapper video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        @media (max-width: 768px) {
            .video-container {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header class="taobao-header">
        <div class="container">
            <div class="logo">淘淘策划</div>
            <nav>
                <ul>
                    <li><a href="index.html">首页</a></li>
                    <li><a href="journey.html">成长历程</a></li>
                    <li><a href="awards.html" class="active">热门活动</a></li>
                    <li><a href="products.html">淘宝好物</a></li>
                    <li><a href="login.html">登录</a></li>
                    <li><a href="register.html">注册</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <div class="awards-container">
        <div class="video-section">
            <div class="video-container">
                <h2>微醺，邂逅浪漫时光</h2>
                <div class="video-wrapper">
                    <video id="video1" autoplay muted loop controls>
                        <source src="img/9f671ef0863c5803f4e02ecdf345f4a3.mp4" type="video/mp4">
                        您的浏览器不支持HTML5视频
                    </video>
                </div>
            </div>
            
            <div class="video-container">
                <h2>寻味东方，沉醉于这杯乌龙茶</h2>
                <div class="video-wrapper">
                    <video id="video2" autoplay muted loop controls>
                        <source src="./img/0412e3fd009cc90a36c2235b2c94bcd2.mp4" type="video/mp4">
                        您的浏览器不支持HTML5视频
                    </video>
                </div>
            </div>
        </div>

        <h1>热门商品推荐</h1>
        <div class="awards-grid">
            <div class="award-item">
                <img src="./img/01.jpg" alt="奶蓟草护旰片辅酶">
                <h3>奶蓟草护旰片辅酶</h3>
                <p>【自营】拜耳OneADay熬夜心肝宝奶蓟草护旰片辅酶Q10护心脏*2瓶</p>
            </div>
            <div class="award-item">
                <img src="./img/02.jpg" alt="长条抱枕">
                <h3>长条抱枕</h3>
                <p>可爱长条抱枕女生睡觉卧室男生款床头大靠垫床上夹腿神器侧睡枕头</p>
            </div>
            <div class="award-item">
                <img src="./img/03.jpg" alt="猫山王榴莲">
                <h3>猫山王榴莲</h3>
                <p>猫山王榴莲新鲜带壳特产应季水果现摘10斤泰国小巴掌顺丰金榴莲枕</p>
            </div>
            <div class="award-item">
                <img src="./img/04.jpg" alt="李宁足球">
                <h3>李宁足球</h3>
                <p>李宁足球专业中考比赛训练成人5号正品四3号儿童4号小学生专用球</p>
            </div>
            <div class="award-item">
                <img src="./img/05.jpg" alt="匹克羽毛球拍">
                <h3>匹克羽毛球拍</h3>
                <p>匹克羽毛球拍官方正品旗舰店超轻全碳素儿童小学生成人单双拍套装</p>
            </div>
            <div class="award-item">
                <img src="img/06.jpg" alt="华硕天选6 Pro">
                <h3>华硕天选6 Pro</h3>
                <p>华硕天选6 Pro酷睿版i7高性能英特尔酷睿HX 16英寸电竞游戏本笔记本电脑</p>
            </div>
        </div>
    </div>

    <footer class="taobao-footer">
        <div class="container">
            <p>© 2025 taotao$$$$$$##@@@@@.</p>
        </div>
    </footer>

    <script src="js/main.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const video1 = document.getElementById('video1');
            const video2 = document.getElementById('video2');
            
            const playPromise1 = video1.play();
            const playPromise2 = video2.play();
            
            // 如果自动播放被阻止，显示播放按钮
            if (playPromise1 !== undefined) {
                playPromise1.catch(error => {
                    video1.controls = true;
                });
            }
            
            if (playPromise2 !== undefined) {
                playPromise2.catch(error => {
                    video2.controls = true;
                });
            }
        });
    </script>
</body>
</html>
