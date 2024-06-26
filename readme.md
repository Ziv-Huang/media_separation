- description
    - 將影片或圖片切割成三等份
    - 解析度比例為16:9，若無法覆蓋的部份以黑邊補足

- python版本: python3.10.7

- output media command:
    - python main.py -v video_name  // 切割影片成三等份
    - python main.py -i image_name  // 切割圖片成三等份
    - python main.py -c video_name -H height -W width // 更改影片解析度
    - python main.py -b video_name  // 將1920*290長條影片下方補黑邊，補到高度為1080

- 捷運橫幅廣告測試
    - 目的：將一般廣告應拉成橫幅螢幕播放(1920*290)，共有三台
    - 方法：
        1. 使用 -c 將影片拉成三台都有涵蓋到的寬度, ex: width: 3600, height: 290
        2. 使用 -b 將影片的下方補黑邊
        3. 使用 -v 將影片切割成三等份


- opencv h264:
    - `sudo apt install build-essential cmake git python3-dev python3-numpy \
        libavcodec-dev libavformat-dev libswscale-dev \
        libgstreamer-plugins-base1.0-dev \
        libgstreamer1.0-dev libgtk-3-dev \
        libpng-dev libjpeg-dev libopenexr-dev libtiff-dev libwebp-dev \
        libopencv-dev x264 libx264-dev libssl-dev ffmpeg`
    - pip install --no-binary opencv-python opencv-python