# Object Detection Resources


There is a file in this directory titled ‘train base’. It’s available to help speed up the process of setting up a trainer. Just modify the values to suit your needs. Copy, Paste, and Go.


Image Datasets

* http://www.vision.ee.ethz.ch/datasets/index.en.html 
* http://www.cvpapers.com/datasets.html 
* http://www.cs.cmu.edu/~cil/v-images.html 
	* Negative Images:
		* svn co http://tutorial-haartraining.googlecode.com/svn/trunk/data/negatives/
			* ~3000 images
		* https://github.com/openalpr/train-detector/tree/master/raw-neg
			* ~3000 images
		* download zip
		* http://www.csee.wvu.edu/~xinl/database.html 
        * `use wget -r -A jpeg,jpg,bmp,gif,png <link>` to pull all the images from a site (may come in handy later)



OpenCV object recognition/training tutorials

Naotoshi Seo’s Tutorial

* http://note.sonots.com/SciSoftware/haartraining.html#w0a08ab4 

Coding Robin Haar Training Tutorial(Personally,my favorite)

* http://coding-robin.de/2013/07/22/train-your-own-opencv-haar-classifier.html
    
Object Training FAQ

* http://www.computer-vision-software.com/blog/2009/11/faq-opencv-haartraining/
    
OpenCV Docs on TrainCascade

* http://docs.opencv.org/doc/user_guide/ug_traincascade.html
    
In-Depth Explanation of Some Parameters

* http://answers.opencv.org/question/7141/about-traincascade-paremeters-samples-and-other/
    
In-depth answers to how to train properly

* http://stackoverflow.com/questions/16058080/how-to-train-cascade-properly
    