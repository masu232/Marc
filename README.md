<h1>Disk Sanitization</h1>


<h2>Description</h2>
Imagine your computer's hard drive or any other storage device (like a USB stick) as a big container where you keep all your files, photos, and videos. Now, sometimes you might want to give away or throw out that container, but you don't want anyone else to see what's inside it.

The disk sanitization program is like a magic tool that makes sure everything inside the container becomes completely unreadable and impossible to recover. It does this by erasing all the information on the storage device and filling it up with either zeros (like writing lots of '0's) or random numbers (like writing down random combinations of numbers).

The program works in three different ways, and you can choose the method you prefer. The first method simply writes '0's all over the container, making it look like a blank slate. The second method is a bit like painting the container with random colors, making it impossible for anyone to understand what was there before. The third method follows a special rulebook to write random numbers over and over again, making sure no one can ever figure out the original content.

Before you run this program, it's crucial to save any important files from the container somewhere safe because once you use the program, everything inside the container will be permanently gone. Once the program finishes its work, it will let you know that the container is now clean, and you can confidently give it away or dispose of it without worrying about anyone peeking into your private stuff.

Remember, this program is like a magic eraser that wipes out all the information on the storage device, so you should be careful when using it and double-check if you're cleaning up the right container. But overall, it's a helpful tool to keep your private data safe when you no longer need the storage device.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python<b>
- <b>shutil<b>

<h2>Environments Used </h2>

- <b>Windows 10 pro</b>

<h2>Program walk-through:</h2>
1. Requirements:

You need Python installed on your system to run the script.
Ensure you have the shutil library, which is usually included with Python by default.
2. Backup Important Data:
Before running the code, ensure you have backed up any important data from the disk you want to sanitize. The script will permanently erase the data on the selected disk.

3. Update Disk Path:
Replace "/path/to/your/disk" with the actual path of the disk you want to sanitize.

4. Select a Method:
Choose the method you want to use for sanitization by setting the sanitization_method variable to one of these options:

"zero-fill": Overwrites data with zeros.
"random-fill": Overwrites data with random values.
"dod-fill": Overwrites data three times following the DoD 5220.22-M standard.

5. Run the Script:
Save the script to a Python file (e.g., disk_sanitization.py) and execute it. Make sure to run it with administrative privileges if needed, as disk sanitization requires low-level access to the disk.
![image](https://github.com/masu232/Marc/assets/141105291/a3e6f975-54c4-4790-b29f-729be9fbe530)
![image](https://github.com/masu232/Marc/assets/141105291/6a423124-842f-4143-bc70-2ef07d8b125c)
![image](https://github.com/masu232/Marc/assets/141105291/fbec4a7d-3380-4df7-ad7c-7e56b02b1cd9)

6. Confirmation:
Once the script finishes execution, it will print "Disk sanitization completed."

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
