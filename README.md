是一款能帮助你管理生活目标的微信小程序。通过 Chronus，你可以轻而易举地对目标进行管理，并且结合计时器能够清楚地去记录你在实现目标过程中的每一条记录。同时他拥有良好的交互体验提供直观的数据分析，帮助你观察目标的进度。

该项目为小程序原生环境开发，并且利用云开发能力（云函数、数据库）作为数据持久化方案，首页的可视化 Pie 使用了[ECharts](https://github.com/ecomfe/echarts-for-weixin)图表。

若你对云开发感兴趣的话，该实践项目可能对你有帮助。



 导入项目

1. 在微信开发工具中导入该项目文件夹。
2. **确保你开通了云开发功能**。
3. 在微信开发工具中将全部云函数上传并部署。
4. 在云开发数据库中创建`users`、`goals`、`goal-records`三个集合。
5. 在`goal-records`中添加`goalId`为唯一索引，在`users`中添加`_openid`为唯一索引。

## 项目结构说明

```
├───cloudfunctions   //云函数存放目录
│   ├───addGoalRecord   //添加目标记录
│   ├───createGoal   //创建目标
│   ├───getGoalData   //获取单个目标信息
│   ├───getGoalList   //获取全部目标
│   ├───login   //注册openid
│   └───removeGoal   //删除单个目标
└───miniprogram   //小程序存放目录
    ├───components   //组件存放目录
    │   ├───loading   //加载组件
    │   ├───tag   //标签组件
    │   └───tips   //提示组件
    │       └───images
    ├───config   //静态配置
    ├───images   //图片资源
    │   ├───detail
    │   ├───home
    │   └───timer
    ├───libs   //引用库
    │   └───ec-canvas
    ├───models
    ├───pages   //页面存放
    │   ├───detail
    │   ├───home
    │   ├───summary
    │   └───timer
    └───utils   //工具函数
```
