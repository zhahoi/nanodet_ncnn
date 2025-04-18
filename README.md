# nanodet_ncnn
基于ncnn框架部署nanodet模型，可以用于实时性较高且性能较差的硬件上的目标检测。



本仓库的代码修改自仓库[ncnn-android-yolov8-seg](https://github.com/Digital2Slave/ncnn-android-yolov8-seg)。原仓库代码部署在安卓端，对于只希望使用yolov8-seg进行实例分割推理的人来说并不直观，因此我把该仓库中和yolov8-seg推理部分的代码提取出来，不依赖android平台即可运行。

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

![微信截图 20240923162656](https://img.picgo.net/2024/09/23/_2024092316265631376e2c7a554cfd.jpeg)

- 图像推理

![微信截图 20240923162558](https://img.picgo.net/2024/09/23/_2024092316255865d26d711182c466.jpeg)



## Reference

- [ncnn-android-yolov8-seg](
