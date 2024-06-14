<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TensorFlow Object Detection Walkthrough</title>
</head>
<body>
    <h1>TensorFlow Object Detection Walkthrough</h1>

    <h2>Steps</h2>

    <h3>Step 1. Create a new virtual environment</h3>
    <pre><code>python -m venv tfod</code></pre>

    <h3>Step 2. Activate your virtual environment</h3>
    <pre><code>.\tfod\Scripts\activate # Windows</code></pre>

    <h3>Step 3. Install dependencies and add virtual environment to the Python Kernel</h3>
    <pre><code>python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfod</code></pre>

    <h3>Step 4. Collect images using the Notebook <em>1. Image Collection.ipynb</em> - ensure you change the kernel to the virtual environment as shown below</h3>
    <img src="https://i.imgur.com/8yac6Xl.png" alt="Kernel Selection">

    <h3>Step 5. Manually divide collected images into two folders train and test.</h3>
    <p>So now all folders and annotations should be split between the following two folders:</p>
    <p>\TFODCourse\Tensorflow\workspace\images\train<br>
    \TFODCourse\Tensorflow\workspace\images\test</p>

    <h3>Step 6. Begin training process by opening <em>2. Training and Detection.ipynb</em></h3>
    <p>This notebook will walk you through installing TensorFlow Object Detection, making detections, saving and exporting your model.</p>

    <h3>Step 8. During this process, the Notebook will install TensorFlow Object Detection.</h3>
    <p>You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.</p>
    <img src="https://i.imgur.com/FSQFo16.png" alt="API Installation Success">

    <p>If not, resolve installation errors by referring to the <em>Error Guide.md</em> in this folder.</p>

    <h3>Step 9. Once you get to step 6. Train the model</h3>
    <p>Inside of the notebook, you may choose to train the model from within the notebook. However, training inside of a separate terminal on a Windows machine allows you to display live loss metrics.</p>
    <img src="https://i.imgur.com/K0wLO57.png" alt="Live Loss Metrics">

    <h3>Step 10. Optionally evaluate your model inside of TensorBoard.</h3>
    <p>Once the model has been trained and you have run the evaluation command under Step 7, navigate to the evaluation folder for your trained model, e.g.</p>
    <pre><code>cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</code></pre>
    <p>and open TensorBoard with the following command:</p>
    <pre><code>tensorboard --logdir=.</code></pre>
    <p>TensorBoard will be accessible through your browser and you will be able to see metrics including mAP (mean Average Precision) and Recall.</p>
</body>
</html>
