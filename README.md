# Blender Cloud Rendering (Google Colab)


## How to use

===> All present GPUs - [K80 < P4 < T4 < P100]  (ascending order in terms of Rendering speed (Slow to Fast))

1) With your Google Account signed in, open Google Drive and create a folder named 'Blender_GC'. Then download and upload 'cloud_render_v5.ipynb' in the same folder.

2) Open the same file from the Drive by double-clicking it which will lead to Google Colaboratory. Go to Edit > Notebook Settings then change Hardware accelerator to GPU and save it with the "omit code cell output when saving this notebook" checked. 

3) Run the first cell to get GPU info. If the GPU is a Tesla K80, you will not be able to use OptiX while rendering so make sure you choose CUDA when asked later.

4) Now run the second cell. First, allow Google Colab to connect to Google Drive. Then select your Google Account and allow it to access files from your Drive.

5) Next, you need to select the Blender installation type. All the selections can be made by entering Item No. Enter '1' if you want it to download and install blender all by itself. Enter '2' if you upload Blender manually. This subtracts the downloading duration every time you run the program. Lastly, enter '3' if you are re-running the program without having it disconnected from the servers and have downloaded and installed Blender already.

6) Here are all the detailed steps for the installation type selection:-
* If '1' is selected, the next table shows all the available Blender versions to download. Again, a particular Blender version can be selected by just entering Item No. After that, Blender will download and then install it on Google Colab servers.
* If '2' is selected, the next table shows all the links of Blender versions to download. One can download any of the versions listed by clicking on the link which will be saved in your downloads. Once it's downloaded, upload the file to the 'Blender_GC' folder created earlier.
Now you can select the version you downloaded and uploaded by the same method from the table (No other Blender versions will be supported other than the ones listed). By this, one skips the downloading part of Blender every time the code is restarted. The application will now be installed on GC's servers.
* If '3' is selected, the download and installation part of the code will be skipped.

7) Next, you can upload the .blend file that you wish to render in that same folder. When the file is done uploading, enter the Blend file name including the file extension. (Example - Test.blend, test.blend1)

8) Now you can select whether you want to use the Cycles Engine or Eevee and if Cycles, use CUDA or OptiX. Remember you cannot select OptiX if the GPU allotted is a Tesla K80.

9) Lastly, select if you wish to render single or multiple frames. If Single frame is selected, you will have to enter the frame number from the blend file. If Animation is selected, one needs to enter the start frame number and then the end frame number. If all the fields entered are valid/correct, the render process will start and the render stats will be shown in the output section. You can find all the rendered frames on Google Drive > Blender_GC > Output. 


## More you Know

1. Free version of Google Colab will allow the user to use GPUs for 12hrs in a week per Google Account. For detailed info, check out  https://colab.research.google.com/signup

2. It's better to provide the Blender Application in your drive as this will subtract the time to download it whenever you run the code in the future.

GLHF ;)

