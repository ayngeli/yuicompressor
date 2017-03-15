# yuicompressor
yuicompressor压缩html、js、css、scss、jsp

方法：Monitoring.init 
初始化基本参数：
suffix ： 压缩的后缀，如min,common.js压缩后为common.min.js，html与jsp不参与
filterDir:过滤目录，正则表达式，如(.*/common/.*)|(.*\\\\common\\\\.*)  为过滤包含common文件夹路径的文件不被压缩
encoding：编码，默认utf-8

方法：Monitoring.startFullCompress
默认启动压缩一次
deleteType：是否压缩后删除文件,针对js\css有效

方法：Monitoring.startWatchJsCssScss
启动监控，会监控当前项目下得所有js\css\html\scss\jsp文件

使用方法：
在项目初始化完成后调用如下信息
Monitoring.init("min", "(.*/common/.*)|(.*\\\\common\\\\.*)");
		Monitoring.startFullCompress(true);
		Monitoring.startWatchJsCssScss(true);
    
    要求：jdk:1.8  
    1.7没有测试
    
    可在测试环境使用1.8，真实环境关闭压缩

如有问题可邮件:leiyang_4050@qq.com
