<br/>

>[!WARNING|style: flat|label:  简要说明 ]
>
><span style='color:Blue'>[ 配置 + 选项 - 表示两个独立的框架 ]</span>
>
>- [ 配置`Configration`] <span style='color:red'>通过一致性的编程方式读取配置数据</span>
>
>- [ 选项`Options`] 借助依赖注入框架实现了`Options 模式` <span style='color:red'>[ 将应用的配置 - 直接注入所需的服务中 ]</span>
>
>---
>
><span style='color:Red'>[ 配置系统 - 核心对象 ]</span>
>
>![image-20221014121958505](/wwwroot/DocImages/image-20221014121958505.png)
>
>- `IConfiguration`<span style='color:Blue'>[ 供客户程序使用 - 读取配置数据 ]</span> <span style='color:red'>[ 配置项：由`键/值对`字符串组成 ]</span>
>- `IConfigurationSource`配置的数据来源(`内存变量, 环境变量, 命令行参数 ... `) 
>
>- `IConfigurationBuilder`<span style='color:red'>主要解决：将不同源提供的数据 → 转换成`IConfiguration`对象</span>
>
>
>---
>
><span style='color:Red'>[ 配置 - 逻辑结构 ]</span>
>
>- (`IConfiguration`) 对象在逻辑上具有一个 <span style='color:red'>[ 树型层次结构 - 称为：配置逻辑树 ]</span>
>
>  [ 原始配置数据：具有多种来源，如内存变量，环境变量，命令行参数等等 ] 
>
> - <span style='color:red'>配置模型的最终目的：提取原始的配置数据 → 并将其转换成`IConfiguration`</span>对象 [ 配置数据从原始结构 → 转变为逻辑结构 ]</span>
>
>
>
><br/>
>
><span style='color:red'>[ 配置由原始结构 → 向逻辑结构的转变 ]</span>
>
>- 原始的配置数据被读取出来后统一转换成 <span style='color:Blue'>[ 字典：中间结构数据 ]</span>
>
>   一颗配置树通过 <span style='color:Blue'>[ 叶节点 ]</span> 承载所有的原子配置项<span style='color:red'> [ 叶节点：由中间字典描述(`Key: 全路径, Value: 配置数据`) ]</span>
>
>
>
>
>![image-20221024161421877](wwwroot/DocImages/image-20221024161421877.png)
>
>
>
><br/>



>
>
>- [<span style='color:#008B00'>[👓 NuGet - Microsoft.Extensions.Configuration.Abstractions ]</span>](https://www.nuget.org/packages/Microsoft.Extensions.Configuration.Abstractions/ ':target=_blank') 
>
>   [<span style='color:#008B00'>[👓 NuGet - Microsoft.Extensions.Configuration ]</span>](https://www.nuget.org/packages/Microsoft.Extensions.Configuration/ ':target=_blank')
>
>  <br/>
>
>- <a href = 'wwwroot/DocUML/v0.html' target='_blank'><span style='color:#008B00'>[👓 UML - 设计图 ]</span></a> [`namespace：Microsoft.Extensions.Configuration`]
>
><br/>
>
>
>











