# <center>Github使用

### 一、注册一个github账号
- 网络好的时候，不需要挂加速器就可以成功注册了

具体流程：
- 填写邮箱，密码，名称，国家
- 人机检测
- 邮箱验证码检测

补充（据说这样可以）：
- 如果挂着加速器不行，可以在完成第一步前，关掉加速器
- 在人机完成前，打开加速器

### 二、配置好环境

（1）下载git

- 可以通过cmd或终端，输入“git --version”来确认是否安装成功

（2）配置git
- 输入“名称”和github的“注册邮箱”
  
可以通过cmd或终端，输入
> git config --global user.name "名称"
> git config --global user.email 邮箱

（3）连接github
- 使用（默认）浏览器使github处于在线状态
- 用VSC连接github
- 注：如果连接不上，可以考虑在终端输入：
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890

> 127.0.0.1:7890 是加速器的默认的地址（127.0.0.1）和端口（7890）。具体还需确认一下更自己的是否一致。

### 三、指令集

|术语           |指令集         |备注
|:---:          |:---:          |:---:
|查看提交记录   |git log        |
|提交           |add 文件全名   |提交一个文件
|推送           |push           |

### 四、相关操作与信息

1. 一些重要的按键在更改右边

2. 更改下面的“消息”框是推送时，发送的信息。注意，可以写入指令。

3. 创建库，由github到VSC：
- 创建文件夹，remote（远程）到github的对应仓库



### 五、多人协作

1. 联动
- 创建私有仓库，并以注册名称或邮箱方式，邀请对方进入
- 在VSC克隆仓库

2. 配置
- “.gitignore” 文件，用于==排除==文件和文件夹
- （这一步由库主来设置）在setting中设置Rules，branch ruleset

Enforcement Status（执行）设置为 Active（启用）

设置Target branches 规则，Add target -> Include by pattern
在默认的基础上，推荐：
Require a pull request before merging -> Required approvals 设置位1

> save时，如果有弹出警告怎么办：对于私有库，需要4美元/月。对于公开库，则不需要。将私有库设置位公开库的方式如下：
> General（在左侧） 中的 Danger Zone（最下面） 中，在Change repository visibility 框内点击 Change visibility -> Change to public

3. 操作

- GRAPH（图像右边的操作）
  
|操作                                |说明
|:---:                               |:---:
|从所有远程存储库中抓取（Fetch）      |读取版本（资料）
|拉取（pull）                        |同步 读取的版本 到本地
|                                    |

- 创建分支

在VSC左下角，鼠标停留，有一个“签出分支/标记”，然后创建一个新的分支

- 并入主干

该分支如果要并入主干，就需要进行PR（pull request）：
在网站的 PR界面 进行==请求==，注意核对分支名字

如果需要==评审==的，可在PR界面“Files changed”中的“Review changes”进行通过

> 邀请同意后，可以在setting（设置）中的Repositories（仓库）中查看：是否进入的仓库

