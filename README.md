# 18675228249.github.io
18675228249.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI数学立体学具 - 二年级学生作品说明卡</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Comic Sans MS', '微软雅黑', sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background-color: #f0f8ff;
            color: #333;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background-color: white;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 25px;
            text-align: center;
        }
        
        h1 {
            margin: 0;
            font-size: 2.2rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }
        
        .subtitle {
            font-size: 1.2rem;
            margin-top: 10px;
        }
        
        .content {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
        }
        
        .left-panel {
            flex: 1;
            min-width: 300px;
            padding: 15px;
        }
        
        .right-panel {
            flex: 1;
            min-width: 300px;
            padding: 15px;
            border-left: 2px dashed #4facfe;
        }
        
        .section {
            margin-bottom: 25px;
            background-color: #f9f9f9;
            border-radius: 15px;
            padding: 15px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        }
        
        h2 {
            color: #4facfe;
            border-bottom: 2px solid #4facfe;
            padding-bottom: 8px;
            font-size: 1.5rem;
        }
        
        h3 {
            color: #ff7e5f;
            font-size: 1.2rem;
        }
        
        ul {
            padding-left: 20px;
        }
        
        li {
            margin-bottom: 8px;
            line-height: 1.5;
        }
        
        .shape-selector {
            display: flex;
            justify-content: space-around;
            margin: 15px 0;
            flex-wrap: wrap;
        }
        
        .shape-btn {
            background-color: #ffb347;
            border: none;
            border-radius: 50%;
            width: 60px;
            height: 60px;
            font-size: 24px;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 3px 5px rgba(0, 0, 0, 0.2);
        }
        
        .shape-btn:hover {
            transform: scale(1.1);
            background-color: #ff7e5f;
        }
        
        .shape-display {
            height: 200px;
            background-color: #f0f8ff;
            border-radius: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 15px 0;
            position: relative;
            overflow: hidden;
        }
        
        .shape {
            width: 120px;
            height: 120px;
            background-color: #4facfe;
            transition: all 0.5s;
        }
        
        .cube {
            transform: rotateX(45deg) rotateY(45deg);
            background-color: #4facfe;
            position: relative;
        }
        
        .cube:before, .cube:after {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 242, 254, 0.7);
            border: 2px solid #4facfe;
        }
        
        .cube:before {
            transform: rotateX(90deg) translateZ(60px);
        }
        
        .cube:after {
            transform: rotateY(90deg) translateZ(60px);
        }
        
        .sphere {
            border-radius: 50%;
            background: radial-gradient(circle at 30% 30%, #4facfe, #00f2fe);
        }
        
        .cylinder {
            border-radius: 50% / 10%;
            background: linear-gradient(to bottom, #4facfe, #00f2fe);
            position: relative;
        }
        
        .cylinder:before {
            content: '';
            position: absolute;
            top: -10%;
            left: 0;
            width: 100%;
            height: 20%;
            background-color: #4facfe;
            border-radius: 50%;
        }
        
        .pyramid {
            width: 0;
            height: 0;
            border-left: 60px solid transparent;
            border-right: 60px solid transparent;
            border-bottom: 120px solid #4facfe;
            background-color: transparent;
            position: relative;
        }
        
        .pyramid:before {
            content: '';
            position: absolute;
            top: 30px;
            left: -60px;
            width: 120px;
            height: 120px;
            background-color: rgba(0, 242, 254, 0.7);
            transform: rotateY(45deg) rotateX(30deg);
        }
        
        .ai-chat {
            background-color: #e6f7ff;
            border-radius: 15px;
            padding: 15px;
            margin-top: 20px;
        }
        
        .chat-box {
            height: 150px;
            overflow-y: auto;
            background-color: white;
            border-radius: 10px;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #4facfe;
        }
        
        .chat-input {
            display: flex;
        }
        
        input {
            flex: 1;
            padding: 10px;
            border: 1px solid #4facfe;
            border-radius: 10px 0 0 10px;
            font-size: 16px;
        }
        
        button {
            background-color: #4facfe;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 0 10px 10px 0;
            cursor: pointer;
            font-size: 16px;
        }
        
        .student-info {
            display: flex;
            align-items: center;
            margin-top: 15px;
        }
        
        .avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: #ffb347;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
            margin-right: 15px;
        }
        
        footer {
            text-align: center;
            padding: 15px;
            background-color: #f0f8ff;
            color: #4facfe;
            font-weight: bold;
        }
        
        @media (max-width: 650px) {
            .content {
                flex-direction: column;
            }
            
            .right-panel {
                border-left: none;
                border-top: 2px dashed #4facfe;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>AI数学立体学具</h1>
            <div class="subtitle">二年级学生作品说明卡</div>
        </header>
        
        <div class="content">
            <div class="left-panel">
                <div class="section">
                    <h2>学具简介</h2>
                    <p>这个AI数学立体学具帮助二年级同学认识不同的立体形状，并通过AI互动加深对几何概念的理解。</p>
                    <p>学具包含了常见的立体形状模型，每种形状都有详细的说明和有趣的互动功能。</p>
                </div>
                
                <div class="section">
                    <h2>形状探索</h2>
                    <p>点击下面的按钮查看不同的立体形状：</p>
                    
                    <div class="shape-selector">
                        <button class="shape-btn" onclick="showShape('cube')">◼️</button>
                        <button class="shape-btn" onclick="showShape('sphere')">🔵</button>
                        <button class="shape-btn" onclick="showShape('cylinder')">🛢️</button>
                        <button class="shape-btn" onclick="showShape('pyramid')">🔺</button>
                    </div>
                    
                    <div class="shape-display">
                        <div class="shape cube" id="shape-display"></div>
                    </div>
                    
                    <div id="shape-info">
                        <h3>正方体</h3>
                        <ul>
                            <li>有6个面，每个面都是正方形</li>
                            <li>所有边长度相等</li>
                            <li>有8个顶点和12条边</li>
                            <li>常见例子：骰子、魔方</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <div class="right-panel">
                <div class="section">
                    <h2>AI助手</h2>
                    <p>向AI助手提问关于立体形状的问题吧！</p>
                    
                    <div class="ai-chat">
                        <div class="chat-box" id="chat-box">
                            <p><strong>AI助手:</strong> 你好！我是数学AI助手。你可以问我关于立体形状的问题，比如"正方体有几个面？"</p>
                        </div>
                        
                        <div class="chat-input">
                            <input type="text" id="user-input" placeholder="输入你的问题...">
                            <button onclick="sendMessage()">发送</button>
                        </div>
                    </div>
                </div>
                
                <div class="section">
                    <h2>学习目标</h2>
                    <ul>
                        <li>认识常见的立体形状（正方体、球体、圆柱体、圆锥体等）</li>
                        <li>了解不同立体形状的特征（面、边、顶点）</li>
                        <li>能够在生活中找到立体形状的例子</li>
                        <li>培养空间想象能力</li>
                    </ul>
                </div>
                
                <div class="section">
                    <h2>制作材料</h2>
                    <ul>
                        <li>彩色卡纸</li>
                        <li>胶水或胶带</li>
                        <li>剪刀</li>
                        <li>尺子</li>
                        <li>电子元件（用于AI功能）</li>
                    </ul>
                </div>
                
                <div class="student-info">
                    <div class="avatar">👧</div>
                    <div>
                        <h3>小设计师</h3>
                        <p>二年级学生</p>
                        <p>热爱数学和创意设计</p>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>AI数学立体学具 - 培养空间思维，探索几何世界！</p>
        </footer>
    </div>

    <script>
        // 显示不同形状的函数
        function showShape(shapeType) {
            const shapeDisplay = document.getElementById('shape-display');
            const shapeInfo = document.getElementById('shape-info');
            
            // 重置形状类
            shapeDisplay.className = 'shape';
            
            // 根据选择的形状添加对应的类
            switch(shapeType) {
                case 'cube':
                    shapeDisplay.classList.add('cube');
                    shapeInfo.innerHTML = `
                        <h3>正方体</h3>
                        <ul>
                            <li>有6个面，每个面都是正方形</li>
                            <li>所有边长度相等</li>
                            <li>有8个顶点和12条边</li>
                            <li>常见例子：骰子、魔方</li>
                        </ul>
                    `;
                    break;
                case 'sphere':
                    shapeDisplay.classList.add('sphere');
                    shapeInfo.innerHTML = `
                        <h3>球体</h3>
                        <ul>
                            <li>没有平面，是一个完全圆滑的形状</li>
                            <li>从中心到表面任何一点的距离都相等</li>
                            <li>没有边和顶点</li>
                            <li>常见例子：篮球、足球、地球仪</li>
                        </ul>
                    `;
                    break;
                case 'cylinder':
                    shapeDisplay.classList.add('cylinder');
                    shapeInfo.innerHTML = `
                        <h3>圆柱体</h3>
                        <ul>
                            <li>有3个面：2个圆形面和1个曲面</li>
                            <li>两个底面是大小相同的圆形</li>
                            <li>没有顶点</li>
                            <li>常见例子：罐头、铅笔、柱子</li>
                        </ul>
                    `;
                    break;
                case 'pyramid':
                    shapeDisplay.classList.add('pyramid');
                    shapeInfo.innerHTML = `
                        <h3>四棱锥</h3>
                        <ul>
                            <li>有5个面：4个三角形面和1个正方形底面</li>
                            <li>有5个顶点和8条边</li>
                            <li>常见例子：埃及金字塔、帐篷</li>
                        </ul>
                    `;
                    break;
            }
        }
        
        // AI聊天功能
        function sendMessage() {
            const userInput = document.getElementById('user-input');
            const chatBox = document.getElementById('chat-box');
            const message = userInput.value.trim();
            
            if (message === '') return;
            
            // 添加用户消息
            chatBox.innerHTML += `<p><strong>你:</strong> ${message}</p>`;
            
            // 模拟AI回复
            let response = getAIResponse(message);
            
            // 添加AI回复
            setTimeout(() => {
                chatBox.innerHTML += `<p><strong>AI助手:</strong> ${response}</p>`;
                chatBox.scrollTop = chatBox.scrollHeight;
            }, 500);
            
            // 清空输入框
            userInput.value = '';
            
            // 滚动到底部
            chatBox.scrollTop = chatBox.scrollHeight;
        }
        
        // 处理AI回复
        function getAIResponse(message) {
            message = message.toLowerCase();
            
            if (message.includes('正方体') || message.includes('立方体')) {
                if (message.includes('几个面') || message.includes('多少面')) {
                    return "正方体有6个面，每个面都是正方形！";
                } else if (message.includes('几个顶点') || message.includes('多少顶点')) {
                    return "正方体有8个顶点！";
                } else if (message.includes('几条边') || message.includes('多少边')) {
                    return "正方体有12条边！";
                } else {
                    return "正方体有6个面、8个顶点和12条边。所有面都是正方形，所有边长度相等！";
                }
            } else if (message.includes('球体') || message.includes('球')) {
                if (message.includes('几个面') || message.includes('多少面')) {
                    return "球体没有平面，它是一个完全圆滑的形状！";
                } else if (message.includes('顶点') || message.includes('边')) {
                    return "球体没有顶点和边！";
                } else {
                    return "球体是一个完全圆滑的形状，没有平面、边和顶点。从中心到表面任何一点的距离都相等！";
                }
            } else if (message.includes('圆柱') || message.includes('圆柱体')) {
                if (message.includes('几个面') || message.includes('多少面')) {
                    return "圆柱体有3个面：2个圆形底面和1个曲面！";
                } else if (message.includes('顶点') || message.includes('边')) {
                    return "圆柱体没有顶点，但是有2条弯曲的边！";
                } else {
                    return "圆柱体有3个面：2个圆形底面和1个曲面，没有顶点，但是有2条弯曲的边！";
                }
            } else if (message.includes('棱锥') || message.includes('金字塔') || message.includes('锥体')) {
                if (message.includes('几个面') || message.includes('多少面')) {
                    return "四棱锥有5个面：4个三角形侧面和1个正方形底面！";
                } else if (message.includes('几个顶点') || message.includes('多少顶点')) {
                    return "四棱锥有5个顶点！";
                } else if (message.includes('几条边') || message.includes('多少边')) {
                    return "四棱锥有8条边！";
                } else {
                    return "四棱锥有5个面、5个顶点和8条边。底面是正方形，侧面是三角形！";
                }
            } else if (message.includes('你好') || message.includes('嗨')) {
                return "你好！我是数学AI助手，很高兴帮助你学习立体形状！";
            } else if (message.includes('谢谢')) {
                return "不客气！继续探索立体形状的奥秘吧！";
            } else {
                return "这个问题很有趣！你可以问我关于立体形状的问题，比如'正方体有几个面？'或'球体有顶点吗？'";
            }
        }
        
        // 允许按回车键发送消息
        document.getElementById('user-input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });
    </script>
</body>
</html>
