# Text_Extraction
## Objective
Perform text extraction from noisy MT samples.
##Dataset
This dataset contains sample medical transcriptions for various medical specialties. https://www.kaggle.com/datasets/tboyle10/medicaltranscriptions

MT Sample with added noise to simulate unclear scanned document.
<img width="144" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/0b38a1e3-390e-40fc-8ba8-464aed2f75d0">

##Details
Dataset given is very raw. We need to annotate manually inorder to use it for training our models. Here we generated line images from the sample and annotated Using PDF plumber and PDF miner to increase the dataset for training.
<img width="205" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/59a819fc-eb0d-4968-bc60-e21a9e173244">
<img width="319" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/c66d495c-05f1-4f6d-ba2e-2cdb7f3402e9">

CRNN architecture is built with MobileNetV3 and ResNet34 as backbones  using PaddleOCR framework. And the model is trained with noisy images. The text recogniser built can be used to extract text from whole document image.

##Results
Output of model, when trained with 50k images
<img width="596" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/08489503-b2fc-4d56-aeac-99f2fbe4f446">

Output of model, when trained with 1L images
<img width="596" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/36e7f69a-8a7e-4148-86bf-88279b69e49b">

Prediction of full document image ,when trained with image size of 32x100
<img width="462" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/e3ee2fa8-95a4-4806-8ff7-f85e5acb9842">
Prediction of full document image ,when trained with image size of 32x320
<img width="556" alt="image" src="https://github.com/varun264/Text_Extraction/assets/78945555/1072618f-46e8-4a60-a675-9abef9b0c0ec">


