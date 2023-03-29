# Kareemer
Kareemer is a neural network aim assist that uses real-time object detection accelerated with CUDA on Nvidia GPUs.
THIS IS A FORKED REPO OF [Lunar](https://github.com/zeyad-mansour/Lunar/) this is not fully made by me, and please dont fall for any scams 

## About

Lunar can be modified to work with a variety of FPS games; however, it is currently configured for Fortnite. Besides being general purpose, the main advantage of using Lunar is that it does meddle with the memory of other processes.

The basis of Lunar's player detection is the [YOLOv5](https://github.com/ultralytics/yolov5) architecture written in PyTorch.

A demo video (outdated) can be found [here](https://www.youtube.com/watch?v=XDAcQNUuT84).

![thumbnail](https://cdn.discordapp.com/attachments/1090244297573539983/1090661489020506162/image.png)

## Installation

1. Install a version of [Python](https://www.python.org/downloads/) 3.8 or later.

2. Navigate to the root directory. Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the necessary dependencies.

```
pip install -r requirements.txt
```

## Usage
```           
python lunar.py
```
To update sensitivity settings:
```           
python lunar.py setup
```
To collect image data for annotating and training:
```           
python lunar.py collect_data
```

## Notes
- The current model is trained on a dataset of Fortnite players, and it will not work well for other games.
- The aimbot is configured to only work when targeting/scoping in (holding down the right mouse button). It works best at a medium/long range.
- There is a known issue that occurs with PyTorch and the GeForce 16 series GPUs on Windows. Unfortunately, if you are using one of these GPUs, the aimbot will not work for you.
- An improved version that is closed-source is currently being developed


## Issues
- The method of mouse movement ([SendInput](https://github.com/zeyad-mansour/Lunar/blob/45e05373036f8bd072667313c155e55735cd7f57/lib/aimbot.py#L126)) is slow. For this reason, the crosshair often lags behind a moving detection. This problem can be lessened by increasing the [pixel_increment](https://github.com/zeyad-mansour/Lunar/blob/45e05373036f8bd072667313c155e55735cd7f57/lib/aimbot.py#L56) (e.g. to 4) so fewer calls to that function are made.
- False positives can also happen under certain lighting conditions.

## Contributing
Pull requests are welcome. If you have any suggestions, questions, or find any issues, please open an [issue](https://github.com/zeyad-mansour/Lunar/issues) and provide some detail.
If you find this project interesting or helpful, please star the repository.

## License
This project is distributed under [GNU General Public License v3.0](https://github.com/zeyad-mansour/Lunar/blob/main/LICENSE) license.
