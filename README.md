## ˵��
1. ʵ����һ�鳣�õ��ļ�����`API`��
2. ��`API`֧�ֶԶ�����̽��в�����
3. Ĭ��ʹ�������[��־ģ��](https://github.com/ShadowThree/dbger)��������ͷ�ļ���ʹ���Լ�����־����ӿڣ�

## ʹ��
1. ͨ��`git submodule add https://github.com/ShadowThree/fatfs_file_handler ThirdUtils/fatfs_file_handler`ָ����Ӵ�ģ�飻
2. ����ͷ�ļ���Դ�ļ���
3. ����洢���ʱ�����
```c
// ���µ� xxxPath/xxxFatFS/xxxFile �����Ѿ��� fatfs.c �ж������
StoreDisk_t sDisk[_VOLUMES] = {
    // path       FATFS       FIL        opt     mCnt
    {SDPath, 	&SDFatFS, 	&SDFile, 	FM_FAT32, 0},		// SDcard disk
    {USERPath, 	&USERFatFS, &USERFile, 	FM_FAT,   0}		// SpiFlash disk
};
```
4. Ȼ��ο�`FH_API_test()`��������ָ�����̽��ж�д������