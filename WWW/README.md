# WWW

## Description
访问Web 页面的简单接口。

这是一个小而实用的获取URL内容的模块。

调用WWW(url)你可以在后台开启下载，然后WWW(url)会返回一个WWW对象。

你可以检测isDone属性来判断下载是否完成或者让步给下载对象，直到下载完成(这样不会阻塞游戏的其他部分)。

如果你想要从web服务器获取数据集成到游戏中：比如最高分列表。同时这也是从下载的图片中创建纹理供web player加载的途径。

WWW 类可以使用GET和POST来请求服务器。WWW类将会使用默认使用GET，如果你提供了postData参数那么会使用POST。

查看： WWWForm 是创建一个合法的postData 参数

注意：传递给WWW 的URLs参数必须转意 % 

注意：http://, https:// 和 file:// 协议在iPhone上支持。ftp:// 协议只支持匿名下载，其他协议不支持匿名。

注意：当在Windows和Windows Store Apps 上使用文件协议访问本地文件的时候，你需要指定 file:///

注意：web player 将有安全沙盒的概念，防止你访问不属于你服务的内容。

```
// Get the latest webcam shot from outside "Friday's" in Times Square
using UnityEngine;
using System.Collections;

public class TestWWW : MonoBehaviour {
	public string url = "https://a.desktopprassets.com/wallpapers/94b2dd745ff4636e3da33de0e5d5d99c40ac6f06/preview_92c873f2-835d-437c-b08f-2332adf19f00.jpg";
	IEnumerator Start() {
		WWW www = new WWW(url);
		yield return www;
		Renderer renderer = GetComponent<Renderer>();
		renderer.material.mainTexture = www.texture;
	}
}
```

## Variables
* assetBundle 一个流式的ab，里面包含了该项目中其他资源
* audioClip 从下载数据中生成的音频片段
* bytes 返回从web 页面获取的二进制数据
* bytesDownloaded 从WWW请求下载的二进制数量
* error 如果下载过程中有错误，返回错误消息
* isDone 下载是否已经结束
* movie 从下载数据中生成的视频片段
* progress 下载的进度
* responseHeaders 返回数据的http 头部 
* text 返回作为字符串
* texture 从下载数据中返回的纹理
* textureNonReadable  从下载数据中返回的不可读的纹理
* threadPriority ab 解压线程的优先级
* uploadProgress 数据上传的进度
* url 请求的url

## Constructors
* WWW 使用给定的URL 创建WWW请求

## Public Functions
* Dispose 销毁WWW对象
* GetAudioClip 返回从下载数据中创建的音频片段
* GetAudioClipCompressed 返回从下载数据中创建的在内存中压缩的音频数据
* LoadImageIntoTexutre 使用下载数据覆盖当前的纹理
    
## Static Functions
* EscapedURL 转义url中的字符
* LoadFromCacheOrDownload 从cache加载指定的版本 ab，如果ab没有cache，将自动瞎子啊然后下载在cache，以便今后从本地获取
* UnEscapedURL 反转义url
