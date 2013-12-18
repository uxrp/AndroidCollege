# Android 开发

## 开发环境搭建
- [安装 ADT](https://developer.android.com/sdk/installing/installing-adt.html)
- [配置 SDK](https://developer.android.com/sdk/installing/adding-packages.html)
- [Ant 编译环境与常用 Ant 命令](https://developer.android.com/tools/building/building-cmdline.html)
- [混淆器](http://developer.android.com/tools/help/proguard.html)

## 常用开发工具
- [genymotion 更快的虚拟机](http://www.genymotion.com/)
- [Android Debug Bridge (ADB)](https://developer.android.com/tools/help/adb.html)
- [使用 DDMS](https://developer.android.com/tools/debugging/ddms.html)
- [Hierarchy Viewer](https://developer.android.com/tools/debugging/debugging-ui.html)
- [使用 logcat 察看日志](https://developer.android.com/tools/help/logcat.html)
- [绘制9点图](https://developer.android.com/tools/help/draw9patch.html)
- [Lint清理无效的资源](http://tools.android.com/tips/lint)
- 逆向工程
	- [android-apktool/](https://code.google.com/p/android-apktool/)
	- [dex2jar](https://code.google.com/p/dex2jar/)
	- [JD-GUI](http://java.decompiler.free.fr/)

## 四大基本组件
- [Activity](http://developer.android.com/reference/android/app/Activity.html)
	- 生命周期与相应方法，四种基本状态 active/paused/stoped/killed
	- 创建: extends Activity
	- 启动: startActivity / startActivityForResult

- [Service](http://developer.android.com/reference/android/app/Service.html)
	- 生命周期与相应方法
	- 创建: extends Service
	- 启动与停止：startService() / stopService() / bindService() / unBindService()

- [BroadcastReceive](http://developer.android.com/reference/android/content/BroadcastReceiver.html)
	- 普通广播 / 有序广播
	- 静态注册与动态注册 registerReceiver
	- 系统广播

- [Content Provider](http://developer.android.com/reference/android/content/ContentProvider.html)
	- query / insert / update / delete

- [Intent](http://developer.android.com/reference/android/content/Intent.html) 和 [Intent Filter](http://developer.android.com/reference/android/content/IntentFilter.html)
	- Intent
		- 显式(指定接收者)与隐式(不指定接收者, component 为空)
		- action. 要执行的动作
		- data. 执行动作所要操作的数据
		- category. 被执行动作的附加信息
		- type. 指定 intent 数据的类型 (MIME type), 例如：intent.setType("text/plain");
		- component. 直接指定 Intent 的目标组件, 例如: intent.setComponent(new ComponentName(MainActivity.this, OtherActivity.class)); 
		- extras. 附加信息, [Bundle](http://developer.android.com/reference/android/os/Bundle.html)
	- Intent Filter
		- action
		- data
		- category
		
	
## 用户界面
- 常用布局
	- [线性布局 Linear Layout](http://developer.android.com/guide/topics/ui/layout/linear.html)
	- [相对布局 Relative Layout](http://developer.android.com/guide/topics/ui/layout/relative.html)
	- [表格布局 Table Layout](http://developer.android.com/guide/topics/ui/layout/grid.html)

- 常用 UI 组件
	- [TextView 类](http://developer.android.com/reference/android/widget/TextView.html)
		- TextView 文本框
		- EditText 可编辑文本框
		- AutoCompleteTextView 自动完成文本框
		- Button 按钮
		- CheckBox 复选框
		- RadioButton 单选按钮
		- ToggleButton 开关按钮
	- [AdapterView 类](http://developer.android.com/reference/android/widget/AdapterView.html)
		- [ListView](http://developer.android.com/reference/android/widget/ListView.html)
		- [GridView](http://developer.android.com/reference/android/widget/GridView.html)
		- [Spinner](http://developer.android.com/reference/android/widget/Spinner.html)
		- [Gallery](http://developer.android.com/reference/android/widget/Gallery.html)
	- [ProgressBar 类](http://developer.android.com/reference/android/widget/ProgressBar.html)
	- [ImageView 类](http://developer.android.com/reference/android/widget/ImageView.html)
	- [菜单 Menus](http://developer.android.com/guide/topics/ui/menus.html)
	- [Action Bar](http://developer.android.com/guide/topics/ui/actionbar.html)
	- [对话框](http://developer.android.com/guide/topics/ui/dialogs.html)
	- [通知](http://developer.android.com/guide/topics/ui/notifiers/notifications.html)
	
## 应用资源

- 位于 res/ 目录

- 资源种类
	- animator 定义 [Property Animation](http://developer.android.com/guide/topics/graphics/prop-animation.html)
	- anim 定义[过渡动画](http://developer.android.com/guide/topics/graphics/view-animation.html#tween-animation)
	- color 定义 [Color State List](http://developer.android.com/guide/topics/resources/color-list-resource.html) 资源
	- drawable 定义 [Drawable Resources](http://developer.android.com/guide/topics/resources/drawable-resource.html)
	- layout 定义[布局资源](http://developer.android.com/guide/topics/resources/layout-resource.html)
	- menu [定义菜单](http://developer.android.com/guide/topics/resources/menu-resource.html)
	- values 简单数据
		- arrays.xml 定义[数组资源](http://developer.android.com/guide/topics/resources/more-resources.html#TypedArray)
		- colors.xml 定义[颜色值](http://developer.android.com/guide/topics/resources/more-resources.html#Color)
		- dimens.xml 定义[尺寸值](http://developer.android.com/guide/topics/resources/more-resources.html#Dimension)
		- strings.xml 定义[字符串](http://developer.android.com/guide/topics/resources/string-resource.html)
		- styles.xml 定义[样式](http://developer.android.com/guide/topics/resources/style-resource.html)
	- xml 原始 xml 资源， 使用 [Resources.getXML()](https://developer.android.com/reference/android/content/res/Resources.html#getXml(int)) 获取
		

## 多线程与异步处理
- [JAVA 线程机制](http://www.cnblogs.com/DreamSea/archive/2012/01/11/JavaThread.html)
- [Handler](https://developer.android.com/reference/android/os/Handler.html)
- [Looper](https://developer.android.com/reference/android/os/Looper.html)
- [Message](https://developer.android.com/reference/android/os/Message.html)
- [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask.html)
- [TimerTask](https://developer.android.com/reference/java/util/TimerTask.html)

## 数据持久化
- [SharedPreferences](http://developer.android.com/reference/android/content/SharedPreferences.html)
	- 键值对
	- 存储基础数据类型
	- 存储位置: /data/data/<包名>/shared_prefs/
	- 使用 [SharedPreferences.Editor](http://developer.android.com/reference/android/content/SharedPreferences.Editor.html) 接口用于修改 SharedPreferences 对象的值

- [SQLite](http://developer.android.com/reference/android/database/sqlite/package-summary.html)
	- [SQLiteOpenHelper](http://developer.android.com/reference/android/database/sqlite/SQLiteOpenHelper.html) 创建和打开数据库
	- [SQLiteDatabase](http://developer.android.com/reference/android/database/sqlite/SQLiteDatabase.html) 操作数据库 (增删改查)


- 文件IO，同传统 Java IO 操作，参加 [java.io](http://developer.android.com/reference/java/io/package-summary.html)

- [Content Provider](http://developer.android.com/reference/android/content/ContentProvider.html)

## 常用库
- [SlidingMenu](https://github.com/jfeinstein10/SlidingMenu) 滑动菜单
- [ViewPagerIndicator](https://github.com/JakeWharton/Android-ViewPagerIndicator) ViewPager 指示器
- [achartengine](https://code.google.com/p/achartengine/) 图表引擎
- [ActionBarSherlock](http://actionbarsherlock.com/) ActionBar 兼容
- [PullToRefresh](https://github.com/chrisbanes/Android-PullToRefresh) 下拉加载


## 常用简写
|简写|全拼|备注|
|---|---|---|
|DDMS|Dalvik Debug Monitor Server|Dalvik调试监控服务器|
|ADB|Android Debug Bridge|Android调试桥|
|NDK|Native Development Kit|Native开发工具包，可以跨平台运行|
