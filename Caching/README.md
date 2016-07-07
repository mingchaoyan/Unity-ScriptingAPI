# Caching

## Description
Caching 类使你可以管理被缓存的ab，使用WWW.LoadFromCacheOrDownload

## Static Variables
* compressionEnabled 控制缓存的数据的压缩，默认打开
* enabled Caching是否打开
* expirationDelay 在ab自动删去前保留的秒数
* maximumAvailableDiskSpace 可以分配给缓存的总字节数
* ready Cache 是否准备好
* spaceFree 当前cache空闲的空间
* spaceOccupied 当前使用掉的空间

## Static Functions
* Authorize 只用于webplayer 
* CleanCache 清理掉由当前应用cache的所有ab
* IsVersionCached 检查指定的ab是否cached
* MarkAsUsed 更新当前cache文件的时间戳
