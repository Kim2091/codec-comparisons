# codec-comparisons
This repo aims to accurately compare different codecs at the same bitrates. Currently it tests NVENC, QuickSync, and CPU encoding.


<details><summary>5000 kbps Comparison</summary>
<p>

FFMPEG Settings: `-c:v h264_nvenc -b:v 5000k -maxrate 5001k -minrate 4999k -bufsize 5000k`

Bitrate: 5000 kbps

Source video: https://mega.nz/file/SBBHWRjL#vl5kkj8WL0Yp26H_xA4QU0O3Flqg78C0EgjRwlTt7wk

| Codec  | Output |
| ------------- | ------------- |
| NVENC H264  | ![NVENC 5000 H264](https://user-images.githubusercontent.com/62084776/214811080-7838e5af-c17e-4ac4-88d7-ec17c3b547b5.png) |
| NVENC HEVC  | ![NVENC 5000 HEVC](https://user-images.githubusercontent.com/62084776/214811174-ee5b74d8-d2b7-452c-bb1d-4639e3caaf35.png) |
| NVENC AV1  | ![NVENC 5000 AV1](https://user-images.githubusercontent.com/62084776/214811215-6c8b942e-85a9-473e-b7cf-f58993ab5504.png) |
| QuickSync AV1  | ![Intel 5000 AV1](https://user-images.githubusercontent.com/62084776/214811266-d9be2cef-332f-461d-9829-e11edfc52d28.png) |
| QuickSync HEVC  | ![Intel 5000 HEVC](https://user-images.githubusercontent.com/62084776/214811303-ed0a5f7c-5dff-42b2-b6d0-f64197fb4f80.png) |
| QuickSync H264  | ![Intel 5000 H264](https://user-images.githubusercontent.com/62084776/214811330-636fafb9-c26e-4fff-ab1b-d433f281bf34.png) |
| CPU H264  | ![CPU 5000 H264](https://user-images.githubusercontent.com/62084776/214811364-56dabe72-e9b0-4511-9781-934c8e0fb890.png) |
| CPU HEVC  | ![CPU 5000 HEVC](https://user-images.githubusercontent.com/62084776/214811396-f5fc4a33-08d0-4186-864e-23d25ff8e792.png) |
| CPU (SVT-AV1) AV1  | ![SVT-AV1 5000](https://user-images.githubusercontent.com/62084776/214811438-f0f01aa0-cf86-4f21-970c-38975e57a7e9.png) |
</p>
</details>
