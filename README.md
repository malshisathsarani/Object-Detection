Tensorflow Object Detection Walkthrough

##Steps

Step 1. Create a new virtual environment

python -m venv tfod
Step 2. Activate your virtual environment

bash
.\tfod\Scripts\activate # Windows 
Step 3. Install dependencies and add virtual environment to the Python Kernel

css
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfod

Step 4. Collect images using the Notebook 1. Image Collection.ipynb - ensure you change the kernel to the virtual environment.

Step 5. Manually divide collected images into two folders: train and test. Now, all folders and annotations should be split between the following two folders:

bash
\TFODCourse\Tensorflow\workspace\images\train
\TFODCourse\Tensorflow\workspace\images\test

Step 6. Begin the training process by opening 2. Training and Detection.ipynb. This notebook will walk you through installing Tensorflow Object Detection, making detections, saving, and exporting your model.

Step 7. During this process, the notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully with the last line stating OK. If not, resolve installation errors by referring to the Error Guide in the repository.

Step 8. Once you get to the step to train the model, you may choose to train the model from within the notebook. However, training inside of a separate terminal on a Windows machine allows you to display live loss metrics.

Step 9. You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command, navigate to the evaluation folder for your trained model, e.g.,

bash
cd Tensorflow/workspace/models/my_ssd_mobnet/eval
and open Tensorboard with the following command:

css
tensorboard --logdir=.
Tensorboard will be accessible through your browser, and you will be able to see metrics including mAP - mean Average Precision, and Recall.
