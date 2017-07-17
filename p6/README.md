###概要###
我选择"泰塔尼克号乘客资料数据集"作为我的数据可视化对象。该数据集包含891名乘客的“生死状况”、“舱位等级”、“姓名”、“性别”、“年龄”等信息。通过数据可视化，读者可以了解究竟哪些因素决定了乘客的生存概率。

###设计###
1.**图表类型**：我在P2项目中已对该数据集进行了分析，我了解到“性别”、“年龄”、“乘客等级”都对乘客的生死有影响。为了能向读者分享我的发现，我选择柱形图“bar chart”来表达数据。柱形图可以方便的对比“不同类别”的事物，比如可以用“两根不同高度的柱子”来代表男女数量的差异。

2.**图表的内容**：我开始想提供6种图表，"Total", "Children", "Adults", "Class1", "Class2","Class3"，后来经别人建议（为方便“各种类群体”比较），我将6个图简化为3个：

- “Total”：全体人员中生还和死亡的人数对比，男女分别统计，并在一张图上显示；
- “Children vs Adults”： 儿童和成人的生还和死亡人数对比，儿童和成人又分为男女；
- “Passenger Class”：一等舱、二等舱、三等舱人员的生还和死亡人数对比，每种等级乘客又分为男女；

3.**视觉编码**：

- x轴、y轴选择：X轴体现是类别，比如“男女”、“儿童和成人”、“乘客等级”，y轴体现的是“各类别成员”生死数量的统计。
- 柱子的**长度**代表人员数量的多少。
- 颜色：蓝色代表“生还”，红色代表“遇难”，这么选择是由于红色有流血的感觉，代表“遇难”比较合适。

4.**布局**：
图表的上方是标题: "Comparison of Number of Titanic Survivors and Victims"，标题下方是图表的“说明”，告诉读者有3种图表可供选择。“说明”下方是“按钮”，未激活的按钮颜色为橙色，激活的按钮颜色为淡蓝色；“按钮”下方是柱形图。网页初始化后显示的是“Total”图表，并且“Total”按钮颜色是激活状态的“淡蓝色”。

5.**图例**：图例在图表的右侧，为方便读者理解，各图的图例统一：蓝色代表“生还”，红色代表“遇难”；

6.**互动**：添加互动按钮，读者可以方便地在三种图表中切换，选择自己感兴趣的内容。

7.**根据反馈意见的修改**：见“反馈”部分。


###反馈###
1）**"朋友1"的反馈**：所有图表的图例颜色代表的内容应该一致，便于读者在各图中切换时，方便理解。

**我是如何改进的**：增加一行代码：mySeries.addOrderRule("Survived",true);可以实现红色代表“遇难者”，蓝色代表“生还者”；

2）**"朋友2"的反馈**：在点击按钮时候，应该出现“小手提示”提高交互体验。

**我是如何改进的**：在程序的开头位置“div.buttons div”中增加CSS样式：“cursor:pointer;”

3）**优达学诚论坛老师的反馈**：https://discussions.udacity.com/t/final-project-thank-you-for-your-suggestion/209639/3

Good job using the tabs to provider readers with different options to visualize the data with. One quick thought is that it might be helpful to consolidate Children with Adults, and combine class 1 through 3 together. So instead of having 6 tabs, you can have 3: Total, Adult vs. Children, and Passenger Class. To accommodate this, you can use grouped bar chart like this2. The benefit is that this allows a convenient and intuitive comparison between the groups, which is really the central insight we want to get out of this dataset.


**我是如何改进的**：我将“儿童”按钮和“成人”按钮合并为一个“儿童VS成人”按钮；合并"一等舱"、“二等舱”和“三等舱”按钮为一个“乘客等级”按钮，同时将图表也合并，方便图表中各组对比。


###资源###
1. dimple.js文档：https://github.com/PMSI-AlignAlytics/dimple/wiki
2. 如何使用github：https://guides.github.com/activities/hello-world/
3. 如何创建block可视化分享：https://bl.ocks.org/-/about
4. 优达学诚论坛可数据视化部分：https://discussions.udacity.com/c/nd002-p6-data-visualization-with-d3-js/sharing-and-feedback


