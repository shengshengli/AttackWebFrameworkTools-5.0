<h1>AttackWebFrameworkTools (For ReadTeam) 使用方法</h1>
<p><a href="https://github.com/Anonymous-ghost/AttackWebFramework"><img alt="Release" src="https://img.shields.io/badge/language-C%23-green.svg" style="max-width:100%;"></a>
<a href="https://github.com/Anonymous-ghost/AttackWebFramework"><img alt="Release" src="https://camo.githubusercontent.com/bffca7fa758d0a778a304f9fce39b8d158297031548577a7b9540e8ad714199b/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f56657273696f6e2d76756c6d617020302e362d79656c6c6f77" data-canonical-src="https://img.shields.io/badge/Version-vulmap 0.6-yellow" style="max-width:100%;"></a>
<a href="https://github.com/Anonymous-ghost/AttackWebFramework"><img alt="Release" src="https://camo.githubusercontent.com/9d35fbd70ef5e0c436c9620c6147aaaa884f26c545fd1ecb924fbda8d4dec4f6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c4943454e53452d47504c2d666636396234" data-canonical-src="https://img.shields.io/badge/LICENSE-GPL-ff69b4" style="max-width:100%;"></a>
<a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/65ed7ba447f5e06f5f1e49164347ccb825afba8eb38af7fad58577e1555fe189/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f7a687a796b65722f76756c6d61703f636f6c6f723d67726565"><img src="https://camo.githubusercontent.com/65ed7ba447f5e06f5f1e49164347ccb825afba8eb38af7fad58577e1555fe189/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f7a687a796b65722f76756c6d61703f636f6c6f723d67726565" alt="GitHub Repo stars" data-canonical-src="https://img.shields.io/github/stars/zhzyker/vulmap?color=gree" style="max-width:100%;"></a>
<a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/2d1ffbd87cd358880d0cf188fb80fa1fce2422eecad072019652dc67bc085f43/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f666f726b732f7a687a796b65722f76756c6d6170"><img src="https://camo.githubusercontent.com/2d1ffbd87cd358880d0cf188fb80fa1fce2422eecad072019652dc67bc085f43/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f666f726b732f7a687a796b65722f76756c6d6170" alt="GitHub forks" data-canonical-src="https://img.shields.io/github/forks/zhzyker/vulmap" style="max-width:100%;"></a></p>
<h2>更新状态日志:</h2>
<ul>
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
（1）缺点不跨平台 poc exp少<br>
（2）优点傻瓜是主要导入url即可实现批量测试,能一键getshell检测绝不sql注入或者不是只检测。其中thinkphp 集成所有rce Exp Struts2漏洞集成了shack2  和k8 漏洞利用工具所有Exp并对他们的exp进行优化和修复。以后尽力融入所有好的利用工具exp和poc全部集成一体!!! 此工具的所集成漏洞全部是基于平时实战中所得到的经验从而写入到工具里。例如:通达oA一键getshell实战测试 struts2一键getshell 等等
</li>
</ul>
<h2>工具使用</h1>
<ul>
AttackWebFrameworkTools 使用说明<br/>
url.txt 中网站一行一个且必须以http:// https:// 开头<br/>
AttackWebFrameworkTools.exe 所有exp都跑<br/>
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
如果会在软件同目录下生产shell.txt。攻击不成功则不会生成
</ul>
<h2>软件使用注意事项</h2>
<ul>
<li>特别注意!!!!如果网站url数量很少10个之内或者20个之内一定要调低线程!!!!!AttackWebFrameworkTools.exe -type thinkphp -thread 5</li>
<li>注意!!!!线程数不要设置太大。线程数越大结果越不准确!!!!!</li>
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
 <li>因为这个是批量不是专项检测工具。比如shiro rce漏洞利用方式需要跑十几个利用链这如果批量检测的话很耗时。不如用专项工具进行检测。<br/>
</li>
</ul>
<h2>上图实测效果</h2>
软件界界面

![menu](https://forum.90sec.com/uploads/default/optimized/2X/c/c8a0333b3c31d28c2db90798d3344dc369965c89_2_898x998.png)<br/>
通达oA一键getshell实战测试注意由于网站数量少所以采用自定义线程数来跑如果采用默认线程那么结果不准确
![tongda](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/tongda.png)<br/>
druid测试批量测试
![druid](https://forum.90sec.com/uploads/default/optimized/2X/a/aa2297c6a09ba219d4d2451b912fc6251e29ae44_2_1380x698.jpeg) 
ApacheFlink实战png
![Apach](https://forum.90sec.com/uploads/default/original/2X/8/85dafde5a3c59063e5877447361d461c47233682.png) 
<h2>注意如果提示软件时间到期可以更改本地时间时间改成2021-02-12-2021-02-30就可以打开软件了</h2>

另外扯点儿别的话题还开发了针对cms进行测试的工具。这款工具等时机成熟会放出来的暂时不放
![menu](https://forum.90sec.com/uploads/default/optimized/2X/b/b04f08fd772ede5e45145b8cf6df3e2c3067acd9_2_1248x1000.png)
收集漏洞
![menu](https://forum.90sec.com/uploads/default/optimized/2X/6/6ea0808a2eebfc7ec8c4b6aac0c4ae8e47bd4759_2_1246x998.jpeg)
测试
![menu](https://forum.90sec.com/uploads/default/optimized/2X/b/b545a978dccb5c41fa1417f2ae0ac5806652e62f_2_1326x1000.jpeg)
solr动图测试
![gif](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/Solr.gif?raw=true)
solr新增exp测试图
![2017](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/solr2017.png)
测试结果
![reslut](https://github.com/Anonymous-ghost/AttackWebFrameworkTools/blob/main/result.png)
