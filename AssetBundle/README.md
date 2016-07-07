# AssetBundle

## Description
AssetBundles 使你可以流式化新增的资源，然后通过WWW类在运行时实例化。AssetBundles 通过BuildPipeline.BuildAssetBundle 来创建。

注意bundle 在平台之间并不兼容，标准平台的ab可以被不是iOS和Android的平台兼容。iOS和Android的bundle 互不兼容。

## Variables

mainAsset 当构建ab的时候指定的主要资源

## Public Functions

* Contains 检查ab中是否含有指定的对象
* GetAllAssetNames 返回ab中所有的资源
* GetAllScenePaths 返回在ab中的所有场景资源的路径
* LoadAllAssets 加载ab中所有指定类型的资源
* LoadAllAssetsAsync 异步加载所有资源
* LoadAsset 从ab中加载指定名字的资源
* LoadAssetAsync 异步从ab中加载指定名字的资源 
* LoadAssetWithSubAssets 从ab中加载资源和子资源
* LoadAssetWithSubAssetAsync 异步加载资源和子资源
* Unload 卸载bundle中的所有资源

## Static Functions
* LoadFromFile 同步从磁盘上的文件加载ab
* LoadFromFileAsync 异步从磁盘上的文件加载ab
* LoadFromMemory 从内存中同步创建ab
* LoadFromMemoryAsync 异步从磁盘山创建ab

## 继承的成员

### Variables
* hideFlags 对象是否被隐藏
* name 对象的名称

### Public Functions
* GetInstanceID 返回实例ID
* ToString  返回对象的名字

### Static Functions
* Destroy 移除一个游戏对象
* DestroyImmediate 快速移除对象，但是推荐使用Destroy
* DontDestroyOnLoad 当加载一个新场景的时候确保游戏对象不销毁
* FindObjectOfType 返回第一个激活的指定类型的对象
* FindObjectsOfTyupe 返回激活的指定类型的对象列表
* Instantiate 克隆一个对象

### Operators
* bool 对象是否存在
* operator != 两个对象是否指向不同对象
* operator == 两个对象是否指向同一个对象
