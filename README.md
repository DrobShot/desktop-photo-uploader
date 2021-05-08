# desktop-photo-uploader
This is a client app built with Electron that allow the user to upload the media content through usb connection between macos/windows computer and ios/android. 

We all know that Ios device are very strict in handling application in ram, infact all the process can operate, when closed in multitasking, for only 3 min.
In this sense we must find a better way to upload tons of file without forcing the user to keep the app open.

In future we can also produce a phone battery charger that contains some kind of rasberry based board that does automatically the upload while charging the device.

As regards Windows users with iPhone must be forced to install iTunes or directly "usbaapl64" and "usbaapl" files provided by apple (Apple Mobile Device USB Driver).
For more information please read https://support.apple.com/it-it/HT204095#PC .
We can include those file in the build and run them when the program is first started with the "shell.openItem(fullPath)" function.


As regards Macos things get a little bit tricky. There isn't an official way to actually mount the visible partition of iPhone.
We can use Fuse, but it require Homebrew and my concern is that the experience might become too complicated for the end-user.
For more information please read https://reincubate.com/it/support/how-to/mount-iphone-files .
Another possibility is to force the user to manually copy the media file to a folder and than load that folder in Electron to do the upload.
The down side of this approach is that we force our user to use Apple Photo, which is a competitor of our service 😅.
Ifuse should get the job done also for Android device in Macos.
For more information please view https://www.youtube.com/watch?v=_jzMiyz4Zt4 .

