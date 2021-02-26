**trunk-based development**

* developer divides their own work into small batches
* merge that work into trunk at least once a day
* Differs from feature branch development:
  * trunk based
    * development typically last no more than a few hours
    * many developers merging their individual changes into trunk frequently
* Developers push code directly into trunk
* Change made in release branch usually merged into trunk asap
* Bug fixed in trunk cherry picked into release
* Benefit: reduce complexity of merging events and keeps code current by having fewer development lines
* it is a required practice for CI



关于前天Tech Huddle时候的基于主干/分支开发的问题：

前者叫Trunk based development，后者叫Git Flow

简单来讲Trunk based是所有人会基于同一个Trunk，也就是main branch，将任务分成小部分，然后切出branch进行小部分开发，当一个小部分完成后就要merge回main里。项目Release要在Release branch上，如果这时候发现了有代码需要修复，则在main上修复后cherry pick到Release里。

另一种叫Gitflow，也就是开始做一个新feature时，会从一个专门用于development的branch切出新Feature branch，直到Feature完成后才合并回development里。合并的时候提交一个PR。再切出一个branch做测试和修复bug。一切完成后再将修复bug的branch合并回development branch，再从dev branch合并回main并打上版本号发布。

Trunk based明显更适合敏捷，而且它也是CI的一个实践。

那Trunk和Gitflow各自适合哪种：

做MVP时/需要加快迭代速度/组里Senior级多。合并不需要PR，采用Trunk效率更高。

开源项目或者团队里Junior较多时，需要确保软件质量，或者团队大/成熟产品，这时需要确保产品稳定性，细微改变都都可能有较大影响，所以需要慎之又慎。这些时候Gitflow可能是一个更好方案。

有人可能要问那Trunk的都没PR了，没review的话代码质量下降的风险岂不是会变大？其实下面谷歌的文章也提出了改进的措施：prioritize code review，避免等几个小时甚至几天后才能review。我认为Pair Programming恰恰是这个问题的一个解决方案。由此再次印证了徐昊那句话------敏捷实践之间是强耦合的。

回到咱们的项目上来，虽然有CI，但是Disbursement更像是采取了Git flow。考虑到项目是与支付相关的，我猜测也是为了更严格的质量把关吧。

参考文章：https://www.toptal.com/software/trunk-based-development-git-flow

https://cloud.google.com/solutions/devops/devops-tech-trunk-based-development



