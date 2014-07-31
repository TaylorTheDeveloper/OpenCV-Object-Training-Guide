# Eclipse, CDT, ADT, NDK, and Android OpenCV Installation for Mobile Dev


Install Eclipse with ADT

* Download:
	* http://developer.android.com/sdk/index.html#download  
	* http://askubuntu.com/questions/318246/complete-installation-guide-for-android-sdk-adt-bundle-on-ubuntu 

CDT

* http://www3.ntu.edu.sg/home/ehchua/programming/howto/eclipsecpp_howto.html

NDK

* Download:
	* https://developer.android.com/tools/sdk/ndk/index.html 
	* https://developer.android.com/tools/sdk/ndk/index.html#Installing
	* http://mindtherobot.com/blog/452/android-beginners-ndk-setup-step-by-step/ 
* Build:
	* http://stackoverflow.com/questions/9988353/building-android-ndk
* ndk-build -C your_project_path

Android OpenCV ( http://docs.opencv.org/java/ )

* Download:
	* http://sourceforge.net/projects/opencvlibrary/files/opencv-android/2.4.9/OpenCV-2.4.9-android-sdk.zip/download 
* Video.java issue:
	* http://answers.opencv.org/question/8266/opencv-library-244-on-eclipse-gives-error/ 
* C++ Build/General Missing from Project Preferences Issue:
	* http://stackoverflow.com/questions/16953548/eclipse-missing-c-c-build-and-general-from-project-properties
* Now, make sure you add NDK root to the build varialbles so you can find that:
	* http://help.eclipse.org/juno/index.jsp?topic=%2Forg.eclipse.cdt.doc.user%2Ftasks%2Fcdt_t_add_build_var.htm
* Finally, to open and run the samples, do this:
	* http://docs.opencv.org/trunk/doc/tutorials/introduction/android_binary_package/dev_with_OCV_on_Android.html#application-development-with-static-initialization 
* Best Practices, brought to you by openCV:
	* http://opencv.org/platforms/android/android-best-practices.html 