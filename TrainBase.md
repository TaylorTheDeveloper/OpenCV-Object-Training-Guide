# Train Base

```Heavily Suggest Reading this, as I’ve found it very useful:

http://coding-robin.de/2013/07/22/train-your-own-opencv-haar-classifier.html

Make Sure you remember to modify the parameters, this file is just for easy access to for rather lengthy comands.

Make Sure you keep notes on the report file.

```

From the root of your training directory:

find ./positive_images -iname "*.jpg" > positives.txt
find ./negative_images -iname "*.jpg" > negatives.txt

perl bin/createsamples.pl positives.txt negatives.txt samples 1100\
  "opencv_createsamples -bgcolor 0 -bgthresh 0 -maxxangle 1.1\
  -maxyangle 1.1 maxzangle 0.5 -maxidev 40 -w 40 -h 40"

cp src/mergevec.cpp ~/opencv-2.4.9/apps/haartraining
cd ~/opencv-2.4.9/apps/haartraining

g++ `pkg-config --libs --cflags opencv` -I. -o mergevec mergevec.cpp\
  cvboost.cpp cvcommon.cpp cvsamples.cpp cvhaarclassifier.cpp\
  cvhaartraining.cpp\
  -lopencv_core -lopencv_calib3d -lopencv_imgproc -lopencv_highgui -lopencv_objdetect

cp mergevec ~/YourDir/
cd ~/YourDIr/

find ./samples -name '*.vec' > samples.txt
./mergevec samples.txt samples.vec


echo "Today is <specify date> " >> report.txt
echo " Write some notes or details about the experiment here. ">> report.txt
echo " " >> report.txt


opencv_traincascade -data classifier -vec samples.vec -bg negatives.txt\
  -numStages 20 -minHitRate 0.995 -maxFalseAlarmRate 0.449 -numPos 3000\
  -numNeg 2000 -w 40 -h 40 -featureType LBP -mode ALL -precalcValBufSize 2048\
  -precalcIdxBufSize 2048 | tee -a report.txt


