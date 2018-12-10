# gitflow-test
gitflow使用
分支

maser，dev 都为长期分支，release, feature, hotfix都是根据实际情况衍生的短期分支。

## 主分支 （master）

始终稳定的分支，主要用于发布生产环境（Production) , 并在相应的版本发布时间点打上相应的版本 tag。 当生产环境出现紧急bug 后，从 master 衍生 hotfix 分支，并进行 bugfix 开发。需要注意的是，master 分支除了与 pre-release 分支有直接的 merge 操作外，不会与 dev 和其他任何 feature 分支进行 merge 操作，除去要进行紧急的 hotfix 分支以外。

## 开发分支（dev）
用于日常正常的开发迭代，大部分的 feature 分支从 dev 衍生，开发完后会合并到dev，并发布到开发测试环境。当开发版本相对稳定，并进入发布日期后，从 dev 衍生 相对应的 pre-release 版本。

## 预发布分支（release branch）

此分支是从 dev 分支衍生，为一个预发布分支，介于 master 与 dev分支之间。主要用于开发测试环境和稳定版本之间的缓冲，主要有以下作用：

+ 清理发布
+ 执行所有测试
+ 更新文档
+ 为下个发布做准备操作
命名规则为：release_版本号， 例如：release_v1.0.0

## 功能分支 （feature branch)

功能特征分支，基于develop分支克隆，主要用于多人协助开发场景或探索性功能验证场景，功能开发完毕后合并到develop分支。feature分支可创建多个，属于临时分支，目的实现后可删除分支。

## 补丁分支 （hotfix branch）

Bug修复分支，基于master分支或发布的里程碑Tag克隆，主要用于修复对外发布的分支，收到客户的Bug反馈后，在此分支进行修复，修复完毕后分别合并到develop分支和master分支。本分支属于临时分支，目的实现后可删除分支。

参考连接 https://blog.csdn.net/zsm180/article/details/75291260
