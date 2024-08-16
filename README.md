## 说明
1. 实现了一组常用的文件操作`API`；
2. 此`API`支持对多个磁盘进行操作；
3. 默认使用了这个[日志模块](https://github.com/ShadowThree/dbger)，可以在头文件中使用自己的日志输出接口；

## 使用
1. 通过`git submodule add https://github.com/ShadowThree/fatfs_file_handler ThirdUtils/fatfs_file_handler`指令添加此模块；
2. 引入头文件和源文件；
3. 定义存储介质变量：
```c
// 以下的 xxxPath/xxxFatFS/xxxFile 变量已经在 fatfs.c 中定义好了
StoreDisk_t sDisk[_VOLUMES] = {
    // path       FATFS       FIL        opt     mCnt
    {SDPath, 	&SDFatFS, 	&SDFile, 	FM_FAT32, 0},		// SDcard disk
    {USERPath, 	&USERFatFS, &USERFile, 	FM_FAT,   0}		// SpiFlash disk
};
```
4. 然后参考`FH_API_test()`函数，对指定磁盘进行读写操作；