## 合作项目主题:sunflower:

有关美国各州的药物中毒分基本情况、地区情况、发展趋势三个方面的可视化及交互

### Pythonanywhere url: [http://vicky923.pythonanywhere.com/](http://vicky923.pythonanywhere.com/)

## 技术文档描述:pushpin:

- **HTML档描述**

分三个页面：[area_situation.html](http://vicky923.pythonanywhere.com/area_situation)、[Basic_situation.html](http://vicky923.pythonanywhere.com/)、[trend_situation.html](http://vicky923.pythonanywhere.com/trend_situation)

功能基本一样，目的是跳转，实现三个主题的不同的下拉框选择

1. area_situation.html和trend_situation.html是以种族来分的，Basic_situation.html是以年份来分，且分别有对应的图，通过数据绑定来实现；

2. 均运用jinja2模板；

3. 图的html档（共有五个）用来python档return render_template进去；

- **Python档描述**

仅有一个app.py文档

1. 读取csv，实现每个页面均有表格且随着下拉选项筛选

2. 自定义函数，render_template -> 图表的显示

3. flask框架的路由@app.route，自定义函数 -> 页面分别为响应前和后，响应前（即下拉框选择前）仅有表格，响应后带图表

- **Web App动作描述**

1. 下拉框，运用数据绑定 -> 实现页面转换，表格随着选项转换，图表转换

2. 导航栏切换页面
