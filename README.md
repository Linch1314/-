<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>智能合同平台 - 首页 (v3)</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
	<link rel="stylesheet" href="./css/dashboard_v2.css">
</head>
<body>
    <div class="top-bar">
        <div class="logo">智能合同平台</div>
        <div class="user-actions"><i class="fas fa-search"></i><i class="fas fa-bell"></i><i class="fas fa-cog"></i><span class="admin-text">admin</span></div>
    </div>
    <div class="main-container">
        <div class="sidebar">
            <ul>
                <li class="active"><a href="dashboard_v2.html"><i class="fas fa-home"></i>首页</a></li>
                <li><a href="templates_v2.html"><i class="fas fa-file-alt"></i>合同模板</a></li>
                <li><a href="draft_v3.html"><i class="fas fa-pencil-alt"></i>合同起草</a></li>
                <li><a href="review_v2.html"><i class="fas fa-shield-alt"></i>合同审查</a></li>
				<li><a href="draft_v3.html"><i class="fas fa-pencil-alt"></i>监督旅行</a></li>
				<li><a href="review_v2.html"><i class="fas fa-shield-alt"></i>信用评价</a></li>
            </ul>
        </div>
        <div class="main-content">
            <div class="breadcrumb"><a href="dashboard_v3.html">首页</a></div>
            <div class="feature-cards">
               
                <a href="draft_v3.html" class="feature-card orange">
                    <i class="fas fa-rocket"></i><span>快速起草</span>
                </a>
                <a href="review_v2.html" class="feature-card pink">
                    <i class="fas fa-tasks"></i><span>智能审查</span>
                </a>
                <a href="templates_v2.html" class="feature-card purple">
                    <i class="fas fa-archive"></i><span>模板库</span>
                </a>
                <a href="#" class="feature-card cyan" onclick="alert('版本管理功能暂未开放'); return false;">
                    <i class="fas fa-history"></i><span>版本管理</span>
                </a>
            </div>
            <div class="stats-overview">
                <div class="stat-card">
                    <div class="stat-card-header"><span class="title">本周起草</span><span class="value">50</span></div>
                    <div class="chart-container"><canvas id="weeklyContractsChart"></canvas></div>
                    <div class="stat-card-footer"><span>较上周 <span class="change">10 <i class="fas fa-arrow-up"></i></span></span></div>
                </div>
                <div class="stat-card">
                    <div class="stat-card-header"><span class="title">本月审查</span><span class="value">120</span></div>
                    <div class="chart-container"><canvas id="monthlyReviewsChart"></canvas></div>
                    <div class="stat-card-footer"><span>较上月 <span class="change green">15 <i class="fas fa-arrow-up"></i></span></span></div>
                </div>
                <div class="stat-card">
                    <div class="stat-card-header"><span class="title">待处理</span><span class="value">8</span></div>
                    <div class="chart-container" style="display:flex; align-items:center; justify-content:center; font-size: 2.8em; color: #0052cc;"><i class="fas fa-exclamation-circle"></i></div>
                    <div class="stat-card-footer"><span>高优先级: 2</span></div>
                </div>
                <div class="stat-card">
                    <div class="stat-card-header"><span class="title">总模板数</span><span class="value">75</span></div>
                    <div class="chart-container" style="display:flex; align-items:center; justify-content:center; font-size: 2.8em; color: #6f42c1;"><i class="fas fa-file-alt"></i></div>
                    <div class="stat-card-footer"><span>新增: 5</span></div>
                </div>
            </div>
            <div class="content-row" style="display: flex; gap: 20px;">
                <div class="content-panel" style="flex:2;">
                    <div class="section-header">
                        <h3>近期活动</h3>
                        <a href="#" class="view-more" onclick="alert('查看全部活动功能暂未开放'); return false;">查看全部</a>
                    </div>
                    <table class="user-activity-table">
                        <thead><tr><th>类型</th><th>合同名称/ID</th><th>操作人</th><th>时间</th><th>状态</th></tr></thead>
                        <tbody>
                            <tr><td>起草</td><td>租赁合同_20230905_001</td><td>张三</td><td>2023-09-05 10:30</td><td><span class="green">已完成</span></td></tr>
                            <tr><td>审查</td><td>服务协议_XYZ</td><td>李四</td><td>2023-09-05 09:15</td><td><span class="orange">进行中</span></td></tr>
                            <tr><td>更新</td><td>保密协议_NDA007</td><td>王五</td><td>2023-09-04 16:00</td><td><span class="green">已完成</span></td></tr>
                            <tr><td>起草</td><td>销售合同_PRE2023008</td><td>赵六</td><td>2023-09-04 11:20</td><td><span class="red">待修改</span></td></tr>
                        </tbody>
                    </table>
                </div>
                <div class="content-panel" style="flex:1;">
                    <div class="section-header"><h3>合同类型分布</h3></div>
                    <div class="chart-area" style="height: 200px;"><canvas id="contractTypeDistributionChart"></canvas></div>
                </div>
            </div>
        </div>
    </div>
    <script src="./js/dashboard_v2.js"></script>
</body>
</html>
