# happiness

本项目由天池发起，使用公开数据的问卷调查结果，选取其中多组变量，包括个体变量（性别、年龄、地域、职业、健康、婚姻与政治面貌等等）、家庭变量（父母、配偶、子女、家庭资本等等）、社会态度（公平、信用、公共服务等等），来预测其对幸福感的评价。详情可以查看https://tianchi.aliyun.com/competition/entrance/231702/information

附件中index文件中包含每个变量对应的问卷题目，以及变量取值的含义。survey文件是数据源的原版问卷，作为补充以方便理解问题背景。

对数据进行特征工程后，利用XGBoost，lightgbm，catboost调参后的结果进行Stacking作为预测值。评价指标用预测值和真实值的均方误差表示。对测试集预测误差最低为0.471，排名64名。
