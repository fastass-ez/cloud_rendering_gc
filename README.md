# cloud_rendering_gc
Blender Files Cloud Rendering by using Google Colab GPUs 
# Cloud Rendering (Google Colab)


## How to use

===> All present GPUs - [K80 < P4 < T4 < P100]  (ascending order in terms of Rendering speed(Slow to Fast))

1. With your Google account signed in on your Web Browser, Open Google Colab - https://colab.research.google.com/notebooks/intro.ipynb#recent=true  and upload 'cloud_render.ipynb' which is a Jupyter Notebook file format provided.

2. Click on Edit > Notebook Settings and change Hardware Accelerator to "GPU" and Enable "Omit code cell output when saving this notebook" option. A reload may be required if it pops up.

3. K80 does not support Optix rendering, so check the GPU connected by running the first line of code. U will have to choose the rendering device (CUDA or OPTIX) later so it's better to decide by having a look at the GPU name.

4. Go to https://download.blender.org/release/  and download the linux64.tar.xz file of the wanted blender version since it only supports Linux 64bit versions. Blender-2.92.0 is used here as an example.

5. Upload the downloaded file to your Google Drive, it is recommended to create a separate folder for the whole cloud render files uploading + downloading.

6. Once uploaded, run the second and the main part of the program. Enter the Authorization code as directed. The first input will be the Blender location that you have downloaded, the location should look like this -  /gdrive/MyDrive/test_render/blender-2.92.0-linux64.tar.xz  , Where 'gdrive/MyDrive/' will be the same for every drive location, 'test_render' is the name of the folder created, and 'blender-2.92.0-linux64.tar.xz' is the name of the uploaded Blender file. This will install Blender.

7. Next, u need to input the blender version, as shown with an example.

8. It will now download some files that may be required for the whole render process.

9. Upload your .blend file to the same folder in your Google Drive.

10. Now, locate the .blend file location in your Google Drive which you want to render. It is recommended to add it in the same folder created for the previous uploads for ease of accessibility. It should look like this - /gdrive/MyDrive/test_render/main.blend  , Where, /gdrive/MyDrive/ are common for all, test_render is the name of the folder, and main.blend is the name of the blender file which is used as an example to be rendered.

11. Now, input the rendering device i.e., "optix" or "cuda", according to GPU availability.

12. Enter the type of render, 's' if u want a specific frame or 'a' if u want an animation/ range of frames to be rendered.

13. If 'a', u will have to input the starting and the ending frame number. If 's', u will just need to enter the single frame number.

14. 'CUDA' type needs a python file to switch from the default settings, so u will have to locate the provided GPU.py file on the same folder if possible. It should look like this - /gdrive/MyDrive/test_render/GPU.py  | *This file isn't needed for the Optix render device.

15) The file will now start to render, it will show current estimates,  etc. similar to the actual rendering scene in Blender.

16) A File will be automatically created named "Output" in the same directory. All rendered files will be visible if it's completed.



## More you Know

1. Free version of Google Colab will allow the user to use GPUs for 12hrs in a week per Google Account. For detailed info, check out  https://colab.research.google.com/signup

2. This only supports Cycles render as for now.

3. If the webpage is closed during the process, it terminates the jupyter notebook file. To make it run in the background, a smartphone can be used for the same, with the tab left open on background processes.



## Sample inputs 

(may vary according to file names  and location)

* Enter directory of blender		      :-  /gdrive/MyDrive/test_render/blender-2.92.0-linux64.tar.xz

* Enter blender version    		      :-  blender-2.92.0-linux64

* Enter directory of blend file to be rendered  :-  /gdrive/MyDrive/test_render/main.blend

* Locate GPU.py file 			      :-  /gdrive/MyDrive/test_render/GPU.py
* 
