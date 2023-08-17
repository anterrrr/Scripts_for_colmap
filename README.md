# Scripts_for_colmap
[colmap](https://github.com/colmap/colmap)是目前最主流的增量式SfM框架  

其重建结果的数据格式通常为3个.bin文件和1个.db文件  
* cameras.bin  
* images.bin
* points3D.bin
* out.db

.bin文件提供重建后的3D点云信息(坐标,rgb,3D和2D对应索引)以及标定后的相机内外参数(images.bin, cameras.bin)详见https://colmap.github.io/index.html

为了更好地呈现重建的可视化效果，在此提供一个改进脚本`visualize_model.py`  

可视化结果如下  
![visualization2](https://github.com/anterrrr/scripts-for-output-from-colmap/assets/130300209/6d601a93-a3d4-49d6-9ebf-c3443041ef2a)
![visualization1](https://github.com/anterrrr/scripts-for-output-from-colmap/assets/130300209/4eb8735d-83dd-49c7-befe-39cd4666742d)
![visualization](https://github.com/anterrrr/scripts-for-output-from-colmap/assets/130300209/0e7d5c9d-36de-49fb-ab2d-e888399cf5c7)  

.db文件提供以下信息:  
* cameras
* images
* keypoints
* descriptors
* matches
* two_view_geometries

为了从.db文件中读取匹配数量,在此提供一个改进脚本`database.py`，其中以双视几何验证(two_view_geometries)后的匹配信息为例运行  
[原始脚本](https://github.com/colmap/colmap/tree/dev/scripts)   

