# Instant-NGP Simple Install Directions
This is a guide for building and running [instant-ngp](https://github.com/NVlabs/instant-ngp) with custom datasets.
Code based on [instant-ngp-helper](https://github.com/comalnik/instant-ngp-helper) with updated directions, protocol, and dependencies.


## Steps
Follow these steps in order -- it matters.


### Setup
1. Install **[Visual Studio Community 2019](https://visualstudio.microsoft.com/vs/older-downloads/#visual-studio-2019-and-other-products)**. Be sure to include `Desktop Development with C++`.
2. Install **[CUDA Toolkit 11.6](https://developer.nvidia.com/cuda-11-6-0-download-archive?target_os=Windows&target_arch=x86_64)**
3. Install **[Anaconda Prompt (Python 3.9)](https://repo.anaconda.com/archive/Anaconda3-2022.05-Windows-x86_64.exe)**
4. Install **[Git](https://git-scm.com/download/win)**
5. Install **[OptiX 7.4.0 SDK](https://developer.nvidia.com/optix/downloads/7.4.0/win64)**
6. Install **[Vulkan SDK](https://vulkan.lunarg.com/sdk/home#windows)**
7. Add **OptiX_INSTALL_DIR** to **System variables** with the value path `C:\ProgramData\NVIDIA Corporation\OptiX SDK 7.4.0`

### Installation
8. Open `Anaconda Prompt` and `cd` to your desired install directory.
9. Type:
```
git clone --recursive https://github.com/ethanproia/instant-ngp-simple
```
10. `cd` into `...\instant-ngp-simple` and run:
```
python install.py
```
11. When install and build are finished, run:
```
pip install opencv-python
```
12. Add `COLMAP` folder to PATH: `C:\Users\[YOUR USERNAME]\...\instant-ngp-simple\COLMAP`


### How to Use
instant-ngp-helper can process both video and image still sequences into NeRFs. 

#### Images
13. Navigate to your `...\instant-ngp-simple\instant-ngp\tmp` directory, make a new folder called `images`, and load your image stills dataset into the `images` folder.
14. In a fresh `Anaconda Prompt`, `cd` into your `instant-ngp-simple` directory and run:
```
python run.py
```
15. Click the `instant-ngp (images)` button in the UI, navigate back to the Anaconda Prompt window and follow the COLMAP instructions. (Don't forget to add the COLMAP folder to PATH as shown in Step 12 or you'll get a COLMAP error.)
16. When COLMAP finishes processing and says `done`, go back to the UI and click `instant-ngp NeRF`.


#### Videos
17. Navigate to your `...\instant-ngp-simple\instant-ngp\tmp` directory and just drop your video file in the folder.
18. In a fresh `Anaconda Prompt`, `cd` into your `instant-ngp-simple` directory and run:
```
python run.py
```
19. Click the `instant-ngp (videos)` button in the UI, navigate back to the Anaconda Prompt window and follow the ffmpeg and COLMAP instructions. (Don't forget to add the COLMAP folder to PATH as shown in Step 12 or you'll get a COLMAP error.)
20. When COLMAP finishes processing and says `done`, go back to the UI and click `instant-ngp NeRF`.


## Video Tutorial
Follow along with my guided video tutorial. (Coming soon)
