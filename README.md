Presentation attacks are a prevalent security concern today. Imposters 
attempt to gain access to restricted resources using fake biometric data such as face, fingerprint, or iris
images. Various presentation attack detection (PAD) systems have
been designed leveraging deep learning (DL) models. But in most
cases, DL models function as black boxes - their decisions are
opaque to their users. The purpose of explainability techniques
is to provide detailed information about the reason behind the
behavior/decision of DL models. Visual explanation is necessary
to better understand the decisions/predictions of DL-based PAD
systems and determine the key regions due to which a biometric
image is considered real or fake by the system. In this work,
a novel technique, Ensemble-CAM, is proposed for providing
visual explanations for the decisions made by deep learning-based
face PAD systems. Our goal is to improve DL-based face PAD
systems by providing a better understanding of their behavior.
Our provided visual explanations will enhance the transparency
and trustworthiness of DL-based face PAD systems.

# The codes can be run on Jupyter Notebook. GPU is needed to run the codes.

Prerequisites:

1. Update your system's package list
   sudo apt update

2. Install pip for python 3 (if not already installed)
   sudo apt install python3-pip

3. Install OpenCV for python
   pip install opencv-python

4. Install numpy
   pip install numpy

5. Install pytorch (for example: CUDA 12.1); 
   pip install torch==2.4.1 torchvision==0.19.1 torchaudio==2.4.1 --index-url https://download.pytorch.org/whl/cu121

6. Install pillow
   pip install pillow

7. Install matplotlib
   sudo apt install python3-matplotlib

8. Install flashtorch
   pip install flashtorch

Ensemble-CAM

This repository provides code for generating and evaluating Class Activation Maps (CAMs) using the Ensemble-CAM approach.
It includes two main Jupyter notebooks:

1. Ensemble_cam.ipynb

This notebook is used to generate CAMs for a single test image.

🔹 Input

Set the path to your test image:

image_path = "Celeba_spoof/test/fake/494514.png"

Set the path to your model:

face_model = "models/facePADceleb_adamW_new.pt"

🔹 Output

The generated CAMs are saved in the output/cams folder:

cam_output_path = os.path.join('output/cams', f'cam_{i+1}.jpg')

File name	& description:
cam_1.jpg: Ensemble-CAM, 
cam_2.jpg: Grad-CAM,
cam_3.jpg: HiResCAM,
cam_4.jpg: Grad-CAM++.

2. Ensemble_cam_evaluation.ipynb

This notebook is used to evaluate the Ensemble-CAM method for the entire test dataset.

🔹 Root Folder

Set the root path containing test image subfolders:

root_folder = "Celeba_spoof/test"


The dependencies can be found here https://github.com/jacobgil/pytorch-grad-cam.  If you need the trained model and dataset, you can email shadmar@clarkson.edu. 
