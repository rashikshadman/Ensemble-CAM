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
a novel technique Ensemble-CAM is proposed for providing
visual explanations for the decisions made by deep learning-based
face PAD systems. Our goal is to improve DL-based face PAD
systems by providing a better understanding of their behavior.
Our provided visual explanations will enhance the transparency
and trustworthiness of DL-based face PAD systems.

# The codes can be run on Jupyter Notebook.

# The Ensemble_cam.ipynb file is used to generate CAMs for a single test image. 

# image_path = "Celeba_spoof/test/fake/494514.png" -- input image path

# cam_output_path = os.path.join('output/cams', f'cam_{i+1}.jpg') -- output folder where generated CAMs are stored; cam_1.jpg is Ensemble-CAM, cam_2.jpg is Grad- CAM, cam_3.jpg is HiResCAM, and cam_4.jpg is Grad-CAM++

# The Ensemble_cam_evaluation.ipynb file is used to evaluate the whole test dataset.

# root_folder = "Celeba_spoof/test" -- folder containing subfolders of images

The dependencies can be found here https://github.com/jacobgil/pytorch-grad-cam.  If you need the trained model and dataset, you can email shadmar@clarkson.edu. 
