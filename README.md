# rasa2_chatbot_medical

## 这个库是什么
Rasa2的版本目前已经release，本库是一个基于rasa2的实例。
在起那面的一个库中 https://github.com/XudongLiu/rasa_chatbot_medical 使用bert训练好的模型，在实践过程中配置较为复杂

这个库使用了rasa默认提供的中文库，在实际测试中，发现还是可以的。

这是一个rasa2的实例

## rasa2的安装过程

rasa2目前使用pip进行安装

`pip3 install rasa==2.0.0rc1 --use-feature=2020-resolver `

目前可以安装正式版本，指定版本即可。

安装过程中可能会被其他的依赖库触发错误，只能根据实际情况解决，或者直接在issue中提出

安装后因为使用中文相关的内容，需要安装spacy，有可能出现的问题及解决方案如下

## 安装spacy过程中可能出现的问题及解决办法

可以参考这个 链接解决 https://www.cnblogs.com/xiaolan-Lin/p/13286885.html

## 如何执行

完成rasa安装后，clone代码

**训练**

`rasa train` 

**执行**

rasa run -m models/20200921-164323.tar.gz --enable-api --cors "*" --debug

**在shell中查看交互过程**

运行custom action：

rasa run actions

运行shell：

rasa shell 

然后就可以进行回答

运行效果如下：
`Your input ->  你好                                                                                      
Hey! How are you?`
`请问您的血糖指数是多少？`
`Your input ->  我的血糖是5.4                                                                             
获取到您的血糖为:5.4`
`Bye`



11月24日更新

本次从新裁剪了story，可以明确的看到在对话中使用slot和custom action获取用户对话数据。通过custom action可以完成自定义的功能，后续将添加neo4j的数据知识库。




## 联系我

Email：343152747@qq.com
If you have any question, please contact me by email or QQ.
