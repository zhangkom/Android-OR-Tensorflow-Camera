# Android-OR-Tensorflow-Camera
This project based on android tensorflow , retrain model to recognize NTD 1,5,10,50 coin

# clone tensorflow source from github to your pc

  https://github.com/tensorflow/tensorflow

# Install tensorflow on your pc

  $pip3 install tensorflow 

# retrain our model to learn from images

  1. gather lots of image (better larger than 20 images of each categories)

    put it in the ~/coin folder

  2. retrain model by using retrain.py

    $cd tensorflow/examples/image_retraining

    $python3 retrain.py --how_many_training_steps=500 --model_dir=/Users/garyhsu/tf_files/model/ --output_graph=/Users/garyhsu/tf_files/retrained_graph.pb --output_labels=/Users/garyhsu/tf_files/retrained_labels.txt --image_dir=/Users/garyhsu/coin

# Optimize the model

    $python3 optimize_for_inference.py --input=/Users/garyhsu/tf_files/retrained_graph.pb --output=/Users/garyhsu/tf_files/optimized_graph.pb --input_names="Mul" --output_names="final_result"


# Demo
https://youtu.be/i1bBcNKei8c


# Reference
https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/#3
https://codelabs.developers.google.com/codelabs/tensorflow-for-poets-2/#2
