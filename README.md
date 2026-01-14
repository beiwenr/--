# 
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>康复大厅拼接地面节点 - 3D与二维详图</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f8fafc;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 25px;
            background: linear-gradient(135deg, #38b2ff 0%, #2a8fd8 100%);
            border-radius: 16px;
            box-shadow: 0 10px 25px rgba(56, 178, 255, 0.2);
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, #38b2ff, #ffffff, #38b2ff);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .subtitle {
            font-size: 1.2rem;
            font-weight: 400;
            opacity: 0.95;
        }
        
        .main-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .model-section {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 16px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            border: 1px solid #e9f7ef;
        }
        
        .section-title {
            background: linear-gradient(135deg, #4caf50 0%, #2e7d32 100%);
            color: white;
            padding: 18px 25px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            font-weight: 600;
            letter-spacing: 0.5px;
        }
        
        .section-title i {
            margin-right: 12px;
            font-size: 1.5rem;
        }
        
        .model-container {
            position: relative;
            width: 100%;
            height: 500px;
            overflow: hidden;
        }
        
        .image-container {
            width: 100%;
            height: 500px;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #f5f9f6;
        }
        
        .image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .info-section {
            width: 100%;
            margin-top: 20px;
        }
        
        .info-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }
        
        .info-box {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 16px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            border: 1px solid #f1e8f7;
        }
        
        .info-box-title {
            background: linear-gradient(135deg, #8e44ad 0%, #6c3483 100%);
            color: white;
            padding: 18px 25px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            font-weight: 600;
            letter-spacing: 0.5px;
        }
        
        .info-box-title i {
            margin-right: 12px;
            font-size: 1.5rem;
        }
        
        .info-content {
            padding: 25px;
        }
        
        h2 {
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            font-size: 1.6rem;
        }
        
        h3 {
            color: #6c3483;
            margin: 25px 0 12px;
            font-size: 1.25rem;
            display: flex;
            align-items: center;
        }
        
        h3 i {
            margin-right: 10px;
            color: #8e44ad;
        }
        
        ul {
            padding-left: 22px;
            margin-bottom: 25px;
        }
        
        li {
            margin-bottom: 12px;
            position: relative;
            padding-left: 10px;
            line-height: 1.7;
        }
        
        li:before {
            content: "•";
            color: #8e44ad;
            font-weight: bold;
            display: inline-block;
            width: 1em;
            margin-left: -1em;
            font-size: 1.3rem;
        }
        
        .process-steps {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 25px;
        }
        
        .step {
            flex: 1;
            min-width: 150px;
            background-color: #f9f4fc;
            padding: 22px;
            border-radius: 12px;
            border-left: 5px solid #8e44ad;
            box-shadow: 0 4px 12px rgba(142, 68, 173, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .step:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(142, 68, 173, 0.15);
        }
        
        .step-number {
            display: inline-block;
            background: linear-gradient(135deg, #8e44ad 0%, #6c3483 100%);
            color: white;
            width: 34px;
            height: 34px;
            border-radius: 50%;
            text-align: center;
            line-height: 34px;
            margin-bottom: 12px;
            font-weight: bold;
            font-size: 1.1rem;
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 20px;
            border-top: 1px solid #e0e6ef;
            color: #7f8c8d;
            font-size: 0.9rem;
            line-height: 1.8;
        }
        
        @media (max-width: 768px) {
            .main-container {
                flex-direction: column;
            }
            
            .model-container, .image-container {
                height: 400px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .info-container {
                flex-direction: column;
            }
        }
        
        @media (max-width: 480px) {
            .model-container, .image-container {
                height: 300px;
            }
            
            .step {
                min-width: 100%;
            }
            
            .info-content {
                padding: 20px 15px;
            }
        }
        
        .loading {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
            font-size: 1.2rem;
            color: #7f8c8d;
        }
        
        .color-palette {
            display: flex;
            justify-content: center;
            margin-top: 15px;
            gap: 10px;
        }
        
        .color-sample {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }
        
        .color-sample.blue {
            background-color: #38b2ff;
        }
        
        .color-sample.green {
            background-color: #4caf50;
        }
        
        .color-sample.purple {
            background-color: #8e44ad;
        }
        
        .image-alt-text {
            text-align: center;
            color: #7f8c8d;
            padding: 20px;
            background-color: #f5f9f6;
            border-radius: 8px;
            margin-top: 10px;
            font-size: 0.9rem;
        }
        
        .sketchfab-embed-wrapper {
            width: 100%;
            height: 100%;
        }
        
        .sketchfab-embed-wrapper iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .sketchfab-embed-wrapper p {
            margin: 0;
            padding: 8px 15px;
            background-color: #f5f9f6;
            font-size: 13px;
            color: #4A4A4A;
            text-align: center;
        }
        
        .sketchfab-embed-wrapper a {
            font-weight: bold;
            color: #1CAAD9;
            text-decoration: none;
        }
        
        .sketchfab-embed-wrapper a:hover {
            text-decoration: underline;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <header>
        <h1><i class="fas fa-layer-group"></i> 康复大厅拼接地面节点</h1>
        <p class="subtitle">3D效果图与二维详图对比及施工指南</p>
        
        <div class="color-palette">
            <div class="color-sample blue" title="天蓝色 - 版头"></div>
            <div class="color-sample green" title="绿色 - 效果图区域"></div>
            <div class="color-sample purple" title="紫色 - 施工信息"></div>
        </div>
    </header>
    
    <main>
        <div class="main-container">
            <div class="model-section">
                <div class="section-title">
                    <i class="fas fa-cube"></i> 3D效果图
                </div>
                <div class="model-container" id="modelContainer">
                    <div class="sketchfab-embed-wrapper">
                        <iframe title="康复大厅拼接地面节点" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/c49b550f1d684ff8be6aa934b76d80df/embed?autospin=1&autostart=1&preload=1">
                        </iframe>
                        <p style="font-size: 13px; font-weight: normal; margin: 5px; color: #4A4A4A;">
                            <a href="https://sketchfab.com/3d-models/c49b550f1d684ff8be6aa934b76d80df?utm_medium=embed&utm_campaign=share-popup&utm_content=c49b550f1d684ff8be6aa934b76d80df" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;">
                                康复大厅拼接地面节点
                            </a>
                            by
                            <a href="https://sketchfab.com/Bo-Zan-Li-Zi?utm_medium=embed&utm_campaign=share-popup&utm_content=c49b550f1d684ff8be6aa934b76d80df" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;">
                                Bo-Zan-Li-Zi
                            </a>
                            on
                            <a href="https://sketchfab.com?utm_medium=embed&utm_campaign=share-popup&utm_content=c49b550f1d684ff8be6aa934b76d80df" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;">
                                Sketchfab
                            </a>
                        </p>
                    </div>
                </div>
            </div>
            
            <div class="model-section">
                <div class="section-title">
                    <i class="fas fa-ruler-combined"></i> 二维详图
                </div>
                <div class="image-container">
                    <img src="https://image2url.com/r2/bucket1/images/1768042522271-499bf818-1b23-4e7c-97b7-888128d01def.png" alt="康复大厅拼接地面节点二维详图" id="floorPlanImage">
                </div>
                <div class="image-alt-text">
                    二维详图展示了地面拼接的详细尺寸、材料标注和施工细节
                </div>
            </div>
        </div>
        
        <div class="info-section">
            <div class="info-container">
                <div class="info-box">
                    <div class="info-box-title">
                        <i class="fas fa-exclamation-triangle"></i> 施工注意事项
                    </div>
                    <div class="info-content">
                        <h3><i class="fas fa-clipboard-check"></i>施工前准备</h3>
                        <ul>
                            <li>确保基层混凝土强度达到C25以上，表面平整无裂缝</li>
                            <li>清除基层表面油污、灰尘、浮浆等杂质</li>
                            <li>检查基层含水率，应低于8%</li>
                            <li>确认施工环境温度在5℃-35℃范围内</li>
                            <li>做好周边区域的保护措施，防止污染</li>
                        </ul>
                        
                        <h3><i class="fas fa-tools"></i>施工中注意事项</h3>
                        <ul>
                            <li>严格按照材料配比进行混合，搅拌时间不少于3分钟</li>
                            <li>涂布材料时应均匀一致，避免局部过厚或过薄</li>
                            <li>施工间隔时间需严格控制，避免层间剥离</li>
                            <li>注意环境湿度变化，必要时采取除湿或加湿措施</li>
                            <li>施工期间保持良好通风，但避免强风直吹表面</li>
                        </ul>
                        
                        <h3><i class="fas fa-tasks"></i>施工后养护</h3>
                        <ul>
                            <li>施工完成后24小时内严禁人员进入</li>
                            <li>养护期间避免水、油等液体接触地坪表面</li>
                            <li>养护温度应保持在10℃以上，避免急剧温度变化</li>
                            <li>完全固化前（一般7天）避免重物碾压或冲击</li>
                            <li>定期检查地坪表面，发现问题及时修补</li>
                        </ul>
                    </div>
                </div>
                
                <div class="info-box">
                    <div class="info-box-title">
                        <i class="fas fa-list-ol"></i> 施工流程
                    </div>
                    <div class="info-content">
                        <div class="process-steps">
                            <div class="step">
                                <div class="step-number">1</div>
                                <h3>基层处理</h3>
                                <p>清理、打磨、修补混凝土基层，确保表面平整牢固</p>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">2</div>
                                <h3>底涂施工</h3>
                                <p>滚涂或刮涂环氧底涂材料，增强附着力</p>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">3</div>
                                <h3>中涂施工</h3>
                                <p>批刮环氧中涂砂浆，填补孔隙增加厚度</p>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">4</div>
                                <h3>面涂施工</h3>
                                <p>滚涂环氧面涂材料，形成平整光滑表面</p>
                            </div>
                        </div>
                        
                        <h3><i class="fas fa-clock"></i>施工时间安排</h3>
                        <ul>
                            <li>基层处理：4-8小时（根据基层状况）</li>
                            <li>底涂施工：2-4小时（干燥时间：8-12小时</li>
                            <li>中涂施工：4-6小时（干燥时间：12-24小时）</li>
                            <li>面涂施工：3-5小时（干燥时间：24-48小时）</li>
                            <li>完全固化：7天后可正常使用</li>
                        </ul>
                        
                        <h3><i class="fas fa-clipboard-list"></i>质量验收标准</h3>
                        <ul>
                            <li>表面平整度：2米直尺检查，缝隙≤3mm</li>
                            <li>表面色泽：均匀一致，无漏涂、气泡、杂质</li>
                            <li>附着力：划格法测试，附着力≥1.5MPa</li>
                            <li>硬度：铅笔硬度≥2H</li>
                            <li>耐磨性：磨耗量≤0.03g（500g/1000转）</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </main>
    
    <footer>
        <p>康复大厅拼接地面节点 © 2023 | 设计制作：Bo-Zan-Li-Zi | 更新时间：2023年11月</p>
        <p>注：本页面展示的3D模型与二维详图仅供参考，实际施工请以现场条件为准。</p>
        <p style="margin-top: 10px; font-size: 0.85rem;">配色方案：版头天蓝色 | 效果图区域绿色 | 施工信息紫色</p>
    </footer>

    <script>
        // 处理图片加载失败的情况
        document.addEventListener('DOMContentLoaded', function() {
            const floorPlanImage = document.getElementById('floorPlanImage');
            floorPlanImage.onerror = function() {
                // 如果图片加载失败，显示替代内容
                const imageContainer = floorPlanImage.parentElement;
                imageContainer.innerHTML = `
                    <div style="text-align: center; color: #7f8c8d; padding: 20px;">
                        <i class="fas fa-drafting-compass" style="font-size: 3rem; margin-bottom: 15px; display: block; color: #4caf50;"></i>
                        <h3 style="color: #2e7d32;">二维详图加载失败</h3>
                        <p>图片URL可能已失效，请联系管理员更新</p>
                        <div style="margin-top: 20px; background-color: #f5f9f6; padding: 15px; border-radius: 8px; text-align: left; border-left: 4px solid #4caf50;">
                            <p><strong>康复大厅拼接地面节点二维详图说明：</strong></p>
                            <p>1. 展示地面拼接的详细构造尺寸</p>
                            <p>2. 包括材料标注、节点大样和施工细节</p>
                            <p>3. 用于施工前的设计确认和技术交底</p>
                        </div>
                    </div>
                `;
            };
            
            // 图片加载成功时添加加载完成提示
            floorPlanImage.onload = function() {
                console.log('二维详图加载成功');
            };
        });
    </script>
</body>
</html>
