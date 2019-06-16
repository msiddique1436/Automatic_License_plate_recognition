# Automatic_License_plate_recognition

This is arguably the best ALPR for Indian traffic as it outperforms most others in the market on Two wheeler and Three wheeler traffic and performs similar if not better for Four wheeler traffic.

This project has 3 main parts 1) Detection of License plates from video footage, 2) Segmentation of characters from extracted License plates, 3) Classification of characters.

### Stage I
For the first stage, I trained a Mobilenet SSD using 14,000 annotated bike and car images, the final terained model can detect and extract license plates from videos with 100% recall. These extracted images of License plates are then passed to the next stage for extraction of individual characters.

### Stage II
For this stage, I wrote my own segmentation algorithm which involved passing the extracted License plates through a series of binarizing filters with various thresholds followed my finding countours. The countours are then sorted and filtered. By the end of this stage we will have each character extracted and stored in an array according to their order on the license plate. What makes this Algorithm different is that it works very robustly for different lightining condition and even when some part of the license plate is covered in shadows, and also that this algorithm works very efficeintly for motor bike and autorickshaw license plates which are 2 lined.


### Stage III
For this stage, I trained two model on a 68,000 dataset of alphanumeric characters the first model was a support vector machine with a linear kernel and the other model was a 5 layered Convolutional neural network. But during production I deployed the SVM model as it was more faster and the accuracy difference between the two models was very less.

### I can't share the code for this project but the above description should be a good starting point for someone wanting to implement this. Below is video of my work in action.


https://www.youtube.com/watch?v=DvYvsZCbrpE

https://www.youtube.com/watch?v=qpO4k03Yac8
