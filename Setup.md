# Setup
SD Maids setup consists of a few steps where you are asked to grant SD Maid certain access and permissions. Some are mandatory, some are not.

## Primary Storage Setup
Primary storage is only required on Android 6.0+ devices. It is necessary because the general read/write permission for public storage can only be aquired during runtime since Android 6.0. Granting these permissions is mandatory as otherwise SD Maid will not function (what good is SD Maid if it can't access any files).
Although ROOT permission superseed any other permission, even on rooted devices it needs to be granted. Trying to skip this step or abort it will close SD Maid.

[[ https://cloud.githubusercontent.com/assets/1439229/14230404/bde057c4-f955-11e5-8050-898550e8e3c0.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230402/bddbf094-f955-11e5-91d6-b7a93e50c46c.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230403/bddc000c-f955-11e5-9b4e-d557fccda9f5.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230401/bddb7ee8-f955-11e5-8197-36870aff4f95.png | height = 300px]]

## Secondary Storage Setup
Secondary storage setup is a step that is only available on Android 5.0+. It's purpose is to grant SD Maid read/write access to storage locations through the system built-in [Android Storage Accessframework (SAF)](http://developer.android.com/guide/topics/providers/document-provider.html).
Since Android 4.4 most devices no longer allow apps to write to the secondary storage (e.g. external/removable sdcards) and accessing sdcards through the SAF only works since 5.0. So sadly Android 4.4 users are out of luck.
Anyways, if you reach this step, SD Maid will display a list of storage locations she would like to be granted access to. Follow these steps:
* Tap an orange entry, remember the location it displays, e.g. `/storage/sdcard1`
* In the newly opened window open the drawer on the left and select the related storage entry
* If there is no entry for your sdcard, close the drawer again, tap the overflow menu button in the top right corner and select `Show sdcards`, then repeat the previous step.
* After selecting the respective storage you should now see it's content in the main window.
* At the top right or bottom right corner, press the select button.
You should now have returned to SD Maid and the previously orange entry is green. Rinse and repeat for every entry.

### Activity not found
The activity through which you grant SD Maid access is part of the "Documents" app, specifically the app with the packagename `com.android.documentsui`. This should be available on any 5.0+ ROM as it is part of the Android Open Source Project (AOSP). If you are getting this error you or someone else modified the ROM such that this app is either not installed or disabled. To check for it's existance you can enable "Show system apps" and then search for the packagename using SD Maids AppControl tool.

### Invalid storage / Invalid input
If you select the wrong storage location (or SD Maid is just not happy with the selection for any reason) you will see and error message and the entry will stay orange. In some cases it is possible that you selected the correct storage and it still said "Invalid" and didn't accept it. Reason for that are usually related to your devices ROM.
(e.g. [#312](../issues/312) or [#231](../issues/231)). As a temporary solution you can permantly skip this step by choosing "Don't show again" from the overflow menu in the top right corner of the setup page and then skipping the step. Although the step is optional not completing it can reduce SD Maids effectiveness. On rooted devices skipping this has less of an impact as SD Maid will fallback to using root for access. Generally SD Maid tries use root only when absolutely necessary because it is usually faster and consumes less resources.

[[ https://cloud.githubusercontent.com/assets/1439229/14230453/787daed6-f958-11e5-9718-be013e87e86e.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230454/7a0150d2-f958-11e5-9c1d-08de69ffad7b.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230455/7b4b0fe6-f958-11e5-9b1a-2bbb5a7d972e.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230457/7f1a8e62-f958-11e5-8713-951b4500f49e.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14230458/7f3ff5b2-f958-11e5-9472-beec5c35c369.png | height = 300px]]
[[ https://cloud.githubusercontent.com/assets/1439229/14256420/51aa30f8-fa99-11e5-9853-5d6b41e4cbbc.png | height = 300px]]