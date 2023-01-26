# codec-comparisons
This repo aims to accurately compare different codecs at the same bitrates. Currently it tests NVENC, QuickSync, and CPU encoding.


<details><summary>5000 kbps Comparison</summary>
<p>

FFMPEG Settings: `-c:v h264_nvenc -b:v 5000k -maxrate 5001k -minrate 4999k -bufsize 5000k`, all other settings are at their defaults

Bitrate: 5000 kbps

Source video: https://mega.nz/file/SBBHWRjL#vl5kkj8WL0Yp26H_xA4QU0O3Flqg78C0EgjRwlTt7wk

| Codec  | H264 | HEVC | AV1 |
| ------------- | ------------- | ------------- | ------------- |
| NVENC | ![NVENC 5000 H264](https://user-images.githubusercontent.com/62084776/214811080-7838e5af-c17e-4ac4-88d7-ec17c3b547b5.png) | ![NVENC 5000 HEVC](https://user-images.githubusercontent.com/62084776/214811174-ee5b74d8-d2b7-452c-bb1d-4639e3caaf35.png) | ![NVENC AV1 5000 (This result is newer than the others)](https://user-images.githubusercontent.com/62084776/214814427-30998c97-f1b8-46eb-8d6d-9a641e577c02.png)
| QuickSync | ![Intel 5000 H264](https://user-images.githubusercontent.com/62084776/214811330-636fafb9-c26e-4fff-ab1b-d433f281bf34.png) | ![Intel 5000 HEVC](https://user-images.githubusercontent.com/62084776/214811303-ed0a5f7c-5dff-42b2-b6d0-f64197fb4f80.png) | ![Intel 5000 AV1](https://user-images.githubusercontent.com/62084776/214811266-d9be2cef-332f-461d-9829-e11edfc52d28.png)
| CPU | ![CPU 5000 H264](https://user-images.githubusercontent.com/62084776/214811364-56dabe72-e9b0-4511-9781-934c8e0fb890.png) | ![CPU 5000 HEVC](https://user-images.githubusercontent.com/62084776/214811396-f5fc4a33-08d0-4186-864e-23d25ff8e792.png) | ![SVT-AV1 5000](https://user-images.githubusercontent.com/62084776/214811438-f0f01aa0-cf86-4f21-970c-38975e57a7e9.png)

Notes: 
  
`The CPU Result above is using SVT-AV1`
  
`Please ignore color differences, this is seemingly an issue with the source clip's color space`
  
`The NVENC AV1 result above is actually newer than the other results. It was re-done based on a newer version of FFMPEG`
</p>
</details>
