# 识别技术债务

每一行代码都可能是技术债务，只要它占用了工程师本该去解决业务上的问题的时间，当然这个时间的问题搞明白了，技术债务的问题也就清晰明了，贵司的业务是什么？工程师主要应该投入到哪里？如果说这两个问题过分笼统，那么我们就再进一步的细细来说：

* 您的团队在干什么？
* 您需要和新加入的同事讲解技术栈吗？
* 您全面更新技术栈的频率是多久？
* 您清楚自己软件的所有依赖吗？
* 什么经常崩掉？
* 处理哪些依赖关系最痛苦？
* 对于所使用的软件栈中的每个组件，替代方案是什么？
* 这些替代方案的项目共同体有多活跃？
* 如果项目共同体消失或停滞不前，需要多少工作来维护该组件？
* 切换这些组件需要耗费多少精力？
* 您的客户或工程师所报告的调试的问题难度有多大？

以上这些问题，可以帮助您理清思绪，开始认真的思考自己的技术债务，以及提醒您平日里忽略的部分。

## 最小化技术债务

我们之所以最大的显性化技术债务，目标的核心是最大限度的减少它，并极力阻止其发展。

### 选择编程语言

用于构建产品的编程语言或开发框架会对开发人员施加某些限制。语言或框架的复杂性越高，就越难维持一支可以与之合作的员工队伍。通常来说，绝大多数时候应选择高级语言[1]，因为这么做的益处是：

* 能够促进招聘，有助于找到更优秀的人才
* 帮助第三方识别和解决问题
* 参与共同体项目，可移植性更高，也变得容易维护
* 对错误的容忍度更高，并允许更简便的解决方案
* 重要文档、教程和预制解决方案的在线来源

### 选择上下游

我们都心知肚明，业务的应用是构建在操作系统、框架和语言等软件栈之上的，这就是应用处于某个生态系统的结构或组成的典型特征，您所选择的上下游系统，将决定技术债务的走向，开发者必须时刻记得要与自己的目标保持一致，举例来说：

* Linux 发行版具有不同的支持条款，并随着时间的推移保证不同级别的API / ABI /安全性。
* 编程语言的选择，要考虑随着时间的推移，运行软件不会受到影响，它会影响在运行时执行代码的能力，并在运行时运行它在其中运行的构建环境不断发展。此外，它可能会限制您寻找新开发人员来管理这些更改的能力。
* 现代语言和框架也倾向于绕过 Linux 发行版的包管理器，自行来打包软件。这个因素可能会像 Linux 发行版一样对您的软件产生长期影响，因此它也应该遵循您的API / ABI /安全需求。

### 选择依赖

世界从未停止发展，开源亦在前行，高质量的开源软件不断问世，而且开源的持续发展，对于组织来说，评估每一个项目都显得至为重要。随着开源自身的增长，会解决很多依赖问题，这也减轻了企业的工作，可以让企业基于此而构建更为复杂的功能和解决方案。

尽管如此，如果某个开源项目的共同体发展不够健康的话，那么就会变成企业的技术债务。所以选择正确的依赖，以及参与到自身依赖的项目共同体亲力亲为，可以通过和他人一起共担来减少技术债务，成就自己的同时也成就他人。

此外，正如我们说软件是一个持续的过程，几年前所依赖的组件是正确的，可能现在未必，换句话说，要持续不断的对依赖进行评估，以确保它在债务最小的状态下为组织效力。

1. 高级编程语言的选择是特定于上下文的，但是，作为此类语言的示例，我们想建议Go，Python，C# 和 Typescript。