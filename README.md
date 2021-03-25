# Easy DAIN for Google Colab

Based in DAIN (Depth-Aware Video Frame Interpolation) by baowenbo and the Colab notebook by btahir.
<br>DAIN: https://github.com/baowenbo/DAIN
<br>Notebook: https://raw.githubusercontent.com/baowenbo/DAIN/master/Colab_DAIN.ipynb

This will install DAIN in your Google Drive (~300MB)
<br>You need to build it once, it takes around 25 minutes. You can find the installer at the bottom of the notebook.
<br>Video processing time depends on video length and resolution. Max video resolution is 720p
<br>I've also added a neat setup feature, where instead of waiting 25 minutes for each runtime, it will save the built packages in your Drive and then import them, it's a lot faster.

## To begin:

* Visit Google Colaboratory (<a href="https://colab.research.google.com/" rel="nofollow">link</a>), go to Github tab and type this repository. 
* Click and open <code>EZ_DAIN_COLAB.ipynb</code>
* You can also save it in your Google Drive.

# Manual
**Setting up DAIN:**

1.   Run 'Setup', connect to your Drive and install dependences on this machine.
2.   Go to 'Installer/Updater' and click run, this will build and save DAIN and it's packages in your Drive. You only need to do it once.
3.   Once built, repeat step **1** every time you connect to a new runtime.

**Running DAIN:**


*   Set the video *input* and *output* path, relative to your Drive root "*My Drive"*
*   Set the output *target framerate* interpolated by DAIN, make sure it's lower than the half of the output framerate. Example: input: 30fps, output: 60fps.
*   For making animated pictures, there's the *Looping* option you can tick, this will use the first frame of the video at the end so it can transition back, closing the loop.
*   If the input has *Audio*, you can tick the checkbox, else don't.
*   When everything is set, run the cell and keep the page alive until processing ends.


**Extra information:**
*   Depending on the video length, resolution and interpolation ratio, the processing time will be long, make sure you're connected to the machine all the way to the end, or at least keeping it active before it shuts down.
*  DAIN lowers the resolution of the video a bit due to deformations in the borders caused by the interpolation process, so it crops it. Is not so noticeable but you can disable/enable it ticking the Resize Hotfix checkbox.
*  If you're using normal Colab (not pro) the runtime time limit you have is **5 hours**, so make sure to split the video into parts or else everything will stop. 
Here's a list of max video length:
   <br> 720p: 4 minutes at 30fps (on Tesla T4)
   <br> 480p: 5.5 minutes at 30fps (on Tesla T4)

**PLEASE NOTE:** The output video speed will be slower than the original, there is a thing i didn't quite understand, it may be the time step or time between frames, but if you have a video editor, speed up the footage to match the original one, use the audio channel separatedly if it has one.

**You can find more information in the colab notebook**

