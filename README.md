# nanodet_ncnn

基于ncnn框架部署nanodet模型，可以用于实时性较高且性能较差的硬件上的目标检测。



本仓库的代码修改自仓库[ncnn-android-nanodet](https://github.com/nihui/ncnn-android-nanodet)。原仓库代码部署在安卓端，对于只希望使用nanodet进行目标检测推理的人来说并不直观，因此我把该仓库中和nanodet推理部分的代码提取出来，不依赖android平台即可运行。

可以对图片和视频流进行推理。



## 依赖库

- opencv-3.4.10

- protobuf-3.4.0
- ncnn-20240820-full-source



##  编译

```sh
mkdir build
cd build
cmake ..
make -j8
```



## 执行

```sh
cd bin
./nanoDet image home/hit/nanodet_ncnn/images/people.jpg    #图片推理
./nanoDet video 0   # 调用摄像头推理
./nanoDet video /home/hit/nanodet_ncnn/images/walkers.mp4  # 调用视频推理
```



## 结果截图

- 调用摄像头推理

![video_detect](https://github.com/zhahoi/nanodet_ncnn/blob/main/docs/video_detect.png)

- 图像推理

![image_detect](https://github.com/zhahoi/nanodet_ncnn/blob/main/docs/image_detect.png)



## Reference

- [ncnn-android-nanodet](https://github.com/nihui/ncnn-android-nanodet)
