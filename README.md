# Cloud Rendering (Google Colab)


## How to use

===> All present GPUs - [K80 < P4 < T4 < P100]  (ascending order in terms of Rendering speed(Slow to Fast))

1. With your Google account signed in on your Web Browser, Open Google Colab - https://colab.research.google.com/notebooks/intro.ipynb#recent=true  and upload 'cloud_render.ipynb' which is a Jupyter Notebook file format provided.

2. K80 does not support Optix rendering, so check the GPU connected by running the first line of code. U will have to choose the rendering device (CUDA or OPTIX) later so it's better to decide by having a look at the GPU name.

3. Run the second, the main part of the program. Enter the Authorization code as directed. First, you need to input whether you want to provide the Blender location or want the Cloud machine to download the file itself, input 'download' for this or 'install', and then provide the path of the downloaded file on your drive. Go to https://download.blender.org/release/ and click on the version you want to render on. Find the linux64.tar.xz type of that particular version as it won't support any other type. 
* If you chose the 'download' option, copy both the link of that page and the version + type, then paste it as an input for the directory. It should look like this - https://download.blender.org/release/Blender2.92/blender-2.92.0-linux64.tar.xz 
* If you chose the 'install' option, download the particular version and upload it to your Google Drive. Now, locate that file from the drive. This should look like this - /gdrive/MyDrive/test_render/blender-2.92.0-linux64.tar.xz  | Here, /gdrive/MyDrive/  will be the same for all as its a common path to get into a Google Drive. 'test_render/' is a folder created, and blender-2.92.0-linux64.tar.xz is the name of the file. 

4. Next, u need to input the blender version, as shown with an example.

5. It will now download some files that may be required for the whole render process.

6. Upload your .blend file to the same folder in your Google Drive.

7. Now, locate the .blend file location in your Google Drive which you want to render. It is recommended to add it in the same folder created for the previous uploads for ease of accessibility. It should look like this - /gdrive/MyDrive/test_render/main.blend  | Where, /gdrive/MyDrive/ are common for all, test_render is the name of the folder, and main.blend is the name of the blender file which is used as an example to be rendered.

8. Now, input the rendering device i.e., "optix" or "cuda", according to GPU availability.

9. Enter the type of render, 's' if u want a specific frame or 'a' if u want an animation/ range of frames to be rendered.

10. If 'a', u will have to input the starting and the ending frame number. If 's', u will just need to enter the single frame number.

11. 'CUDA' type needs a python file to switch from the default settings, so u will have to locate the provided GPU.py file on the same folder if possible. It should look like this - /gdrive/MyDrive/test_render/GPU.py  | *This file isn't needed for the Optix render device.

12) The file will now start to render, it will show current estimates,  etc. similar to the actual rendering scene in Blender.

13) A File will be automatically created named "Output" in the same directory. All rendered files will be visible if it's completed.



## More you Know

1. Free version of Google Colab will allow the user to use GPUs for 12hrs in a week per Google Account. For detailed info, check out  https://colab.research.google.com/signup

2. This only supports Cycles render as of now.

3. If the webpage is closed during the process, it terminates the Jupyter notebook file. To make it run in the background, a smartphone can be used for the same, with the tab left open on background processes.

4. It's better to provide the Blender Application in your drive as this will subtract the time to download it whenever you run the code in the future.



## Sample inputs 

(may vary according to file names  and location)

* Enter directory of Blender  (Google Drive)	:-  /gdrive/MyDrive/test_render/blender-2.92.0-linux64.tar.xz

* Enter Blender Download path link              :-  https://download.blender.org/release/Blender2.92/blender-2.92.0-linux64.tar.xz

* Enter blender version    		        :-  blender-2.92.0-linux64

* Enter directory of blend file to be rendered  :-  /gdrive/MyDrive/test_render/main.blend

* Locate GPU.py file 			        :-  /gdrive/MyDrive/test_render/GPU.py
 

GLHF ;)

