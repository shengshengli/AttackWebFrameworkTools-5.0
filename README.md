  <h1>注意:<br/>
  切勿利用本工具对未授权的网站进行非法攻击。由此产生的法律后果由使用者自行承担!!!</h1>
  <h1>AttackWebFrameworkTools 1.0 2021-03-06</h1>
  
 ![menu](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/menu.png)
 <h1>AttackWebFrameworkTools For RedTeam </h1>
<p><a href="https://github.com/Anonymous-ghost/AttackWebFrameworkTools"> <img alt="Author" src="https://img.shields.io/badge/Author-Anonymousghost-red" style="max-width:100%;"></a>
  <a href="https://github.com/Anonymous-ghost/AttackWebFrameworkTools"> <img alt="Version" src="https://img.shields.io/badge/AttackWebFrameworkTools-Version1.0-faa755" style="max-width:100%;"></a>
  <a href="https://github.com/Anonymous-ghost/AttackWebFrameworkTools"> <img alt="type" src="https://img.shields.io/badge/type-bin-blueviolet" style="max-width:100%;"></a>
  <a href="https://github.com/Anonymous-ghost/AttackWebFrameworkTools"><img alt="Release" src="https://img.shields.io/badge/language-C%23/C++-ff69b4.svg" style="max-width:100%;"></a>
<a target="_blank" rel="noopener noreferrer"><img  alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Anonymous-ghost/AttackWebFrameworkTools?color=gree" style="max-width:100%;"></a>
<a target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/github/forks/Anonymous-ghost/AttackWebFrameworkTools" style="max-width:100%;"></a></p>
<h2>更新状态日志:</h2>
<ul>
  <li>2021-03-12> 编译了最新版本的ysoserial java反序列化漏洞利用工具。并且增加测试类下载地址:外链:https://wwa.lanzous.com/b09xsbzuh 密码:g80i</li>
 <li>2021-03-06 新增DVR 摄像头exp 新增Nexus Repository Manager exp。修改默认线程数为20。增加超时时间。增加界面显示shell的路径。修复cookie bug</li>
 <li>2021-03-03 修复某些类延时时间过短导致漏洞检测不准确。下一个版本将调整默认线程数字预计是20或者10</li>
 <li>2021-02-27 新增 CVE-2021-21972 Vmware vcenter exp</li>
 <li>2021-02-24 修复thinkphp某处rce不能测试成功的bug</li>
 <li>2021-02-21 新增fastjson jenkins  exp/poc </li>
 <li>2021-02-20 新增ElasticSearch  exp/poc </li>
 <li>2021-02-19 新增Drupal  exp/poc </li>
 <li>2021-02-16 新增tomcat unomi exp/poc </li>
 <li>2021-02-15 新增activemq exp/poc </li>
 <li>2021-02-14 新增solr exp/poc 结果增加了cve编号和漏洞名称</li>
 <li>2021-02-12 更新solr 4个exp/poc 动图测试效果见本页底部</li>
 <li>2021-02-08 更新solr CVE-2019-17558 一个CVE</li>
 <li>2021-02-05 更新Dlink</li>
 <li>2021-02-01 更新apachedruid</li>
 <li>.......</li>
 </ul>
<h2>工具编写背景:</h2>
<ul>
<li>编写目的：<br>
测试已经公开漏洞
</li>
<li>背景<br>
在公司内部有些早已经公开的漏洞比如struts2 thinkphp weblogic 这些需要批量测试用网上的工具有C#写的有python java 写的用这些工具都得装一下依赖库。python虽然很方面但是装库确实是很麻烦。另外本人也不擅长python。java可以可以跨平台但是java jdk 之间相互不兼容。另外java我没有.net擅长。go语言新崛起的语言听说是高并发很不错但是我不会 。另外外编译生成文件太大(主要是因为不会手动滑稽)。还是最后选择.net来编写
</li>
<li>优点缺点<br>
（1）缺点:不跨平台 poc exp少<br>
（2）优点:本软件首先集成危害性较大前台rce(无需登录,或者登录绕过执行rce)。反序列化(利用链简单)。上传getshell。sql注入等高危漏洞直接就可以拿权限出数据。其次对一些构造复杂exp漏洞进行检测。傻瓜式主要导入url即可实现批量测试,能一键getshell检测绝不sql注入或者不是只检测。其中thinkphp 集成所有rce Exp Struts2漏洞集成了shack2  和k8 漏洞利用工具所有Exp并对他们的exp进行优化和修复。以后尽力融入所有好的利用工具exp和poc全部集成一体!!! 此工具的所集成漏洞全部是基于平时实战中所得到的经验从而写入到工具里。例如:通达oA一键getshell实战测试 struts2一键getshell 等等
</li>
</ul>
<h2>AttackWebFrameworkTools工具使用方法</h1>
<ul>
AttackWebFrameworkTools 使用说明<br/>
url.txt 中网站一行一个且必须以http:// https:// 开头<br/>
AttackWebFrameworkTools.exe 所有exp都跑使用默认线程模式<br/>
  AttackWebFrameworkTools.exe  -thread 200 所有exp都跑使用自定义线程模式<br/>
AttackWebFrameworkTools.exe -type thinkphp 使用默认线程跑 thinkphp框架漏洞使用说明<br/>
AttackWebFrameworkTools.exe -type thinkphp -thread 200 使用自定义线程 线程跑 thinkphp框架漏洞<br/>
集成漏洞如下(-type参数) <br/>
thinkphp<br/>
weblogic<br/>
struts2<br/>
hadoop<br/>
atlassiancrowd<br/>
ueditor<br/>
tongdaoa<br/>
apacheflink<br/>
ruijie<br/>
apachedruid<br/>
dlink<br/>
solr<br/>
activemq<br/>
tomcat<br/>
unomi<br/>
drupal<br/>
es<br/>
fastjson<br/>
jenkins<br/>
vmvcenter<br/>
webcam<br/>
nexus<br/> 
如果会在软件同目录下生产shell.txt。攻击不成功则不会生成。DVR 如果跑出来密码是空的那么说明不需要密码只要用户名登陆即可。注意webcam为摄像头漏洞合集类如果以后摄像头有新漏洞那么就在webcma这个参数里面
</ul>
<h2>软件使用注意事项</h2>
<ul>
 <li>切勿利用本工具对未授权的网站进行非法攻击。由此产生的法律后果由使用者自行承担!!!</li>
<li>特别注意!!!!如果网站url数量很少10个之内或者20个之内一定要调低线程!!!!!AttackWebFrameworkTools.exe -type thinkphp -thread 5</li>
<li>再次特别注意(非常非常重要):线程数不要设置太大。线程数越大结果越不准确!!!!!。会漏洞某些有漏洞的网站所以一定要调低线程!!!一定要调低线程!!!</li>
<li>非回显漏洞采用dnslog 验证确保联网。如果在局域网不联网环境下dnslog验证的漏洞全部无法验证。
</li>
<li>遇到postData是jason格式时候必须 Content-type:application/json 而不是默认格式<br/></li>
<li>Dlink漏洞需要有AttackWebFrameworkTools.exe.config 并且一个网站一分钟内最多可以检测三次超过三次即使漏洞存在也检测不到 这个目前反弹shell方式不清楚<br/></li>
<li>solr CVE-2017-12629 漏洞检测时间耗时较长请耐心等待结果</li>
<li>建议进行针对对性漏洞测试全量跑耗时就容易被waf封<br/></li>
<li>切勿使用工具对网站进行未授权非法攻击,由此一切产生的后果与作者无关!!!!</li>
<li>为了避免被非法利用工具软件最大支持检测url个数为1千条</li>
<li>另外说如果有合适的exp或者poc可以联系我邮箱Anonymous-ghost@qq.com。另外如果有bug或者好的建议也可以把意见发送到我的邮箱。一起携手打造web框架自动化测试工具</li>
</ul>
<h2>为什么有的框架集成了部分漏洞,为什么有的框架漏洞没有集成</h2>
<ul>
 <li>因为这个是批量不是专项检测工具。有的漏洞利用链很复杂要调用外部程序生成payload进行检测。很耗时另外有的exp或者poc只针对特定版本。不同版本exp不同。无法确定版本的时候导致很难准确进行漏洞检测和利用。故暂时没有集成。未来可能会考虑集成!!!<br/>
</li>
</ul>
<h2>上图实测效果</h2>
CVE-2021-21972 Vmware vcenter 最新漏洞测试结果

![vmwareVcenter](https://forum.90sec.com/uploads/default/optimized/2X/1/12089d8e835bf4c75f7f6f2001472c25a929cc78_2_1380x680.png)<br/>
windows主机测试
![vmwareVcenter-windows](https://forum.90sec.com/uploads/default/optimized/2X/7/7271f9719369cdac95e1706a31eb402443cee3df_2_1380x868.png)<br/>

通达oA一键getshell实战测试注意由于网站数量少所以采用自定义线程数来跑如果采用默认线程那么结果不准确

![tongda](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/tongda.png)<br/>
druid测试批量测试
![druid](https://forum.90sec.com/uploads/default/optimized/2X/a/aa2297c6a09ba219d4d2451b912fc6251e29ae44_2_1380x698.jpeg) 
ApacheFlink实战png
![Apach](https://forum.90sec.com/uploads/default/original/2X/8/85dafde5a3c59063e5877447361d461c47233682.png) 
ActiveMQ测试
![ActiveMQ](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/ActiveMQ.png)
solr动图测试
![gif](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/Solr.gif?raw=true)
solr新增exp测试图
![2017](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/solr2017.png)
测试结果
![reslut](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/result.png)
同类软件Unomi测试对比:某软件测试结果速度有点慢可能是线程开的小
![unomi](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/UnoM.png)
我们的软件测试结果和速度几分钟搞定
![myunomi](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/UnomiMysoft.png)

<h2>注意如果提示软件时间到期可以更改本地时间时间改成软件当前时间加半个月时间之内例如:2021-02-19 那么把本地时间改成2021-02-19-2021-03-06之间的时间就可以打开软件了</h2>
另外扯点儿别的话题还开发了针对cms进行测试的工具。这款工具等时机成熟会放出来的暂时不放

![menu](https://forum.90sec.com/uploads/default/optimized/2X/b/b04f08fd772ede5e45145b8cf6df3e2c3067acd9_2_1248x1000.png)
收集漏洞
![menu](https://forum.90sec.com/uploads/default/optimized/2X/6/6ea0808a2eebfc7ec8c4b6aac0c4ae8e47bd4759_2_1246x998.jpeg)
测试
![menu](https://forum.90sec.com/uploads/default/optimized/2X/b/b545a978dccb5c41fa1417f2ae0ac5806652e62f_2_1326x1000.jpeg)

