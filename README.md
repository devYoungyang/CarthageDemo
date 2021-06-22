# CarthageDemo
##### carthage管理三方库

###### 使用Carthage安装依赖

#### 1.进入项目所在文件夹

`cd /项目路径`

#### 2.创建一个Carthage文件

`touch Carthage`

#### 3.使用Xcode打开Cartfile文件

`open -a Xcode Cartfile`

#### 4.编辑Carthage文件安装所需依赖

`github "SwifterSwift/SwifterSwift" ~> 5.2.0`

#### 5.执行命令

`carthage update  --platform iOS`

#### 6.添加framework到项目中

###### 点击项目名称 -> TARGETS  -> General 底部找到 Frameworks,Libraries,andEmbedded Content

###### 点击+ 选择Add Other 选择项目下 Carthage/Build/iOS/SwifterSwift.framework  添加到工程中

#### 7.选择Build Phases

###### 点击左上角+ 添加 New Run Script Phase

#### 8.点击 Input Files 下面的 + 号为每一个 framework 添加访问路径

`$(SRCROOT)/Carthage/Build/iOS/SwifterSwift.framework`

#### 9.引入三方库，并编译项目成功就可以使用了

`**import** SwifterSwift`

