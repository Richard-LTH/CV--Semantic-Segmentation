Readme

Introduction

This project uses datasets from five folders: K-01, K-03, V-01, V-02, V-03. (Download the file using the link provided in the Ed forum.)
Each processing step is strongly correlated with the previous one. To only run the test code ("test_on_deeplab".ipynb and "test_on_segformer.ipynb"), ensure a folder named dataset (contains folders K-01, K-03, V-01, V-02, V-03) in the same directory (which contains all the data images) and their corresponding label files. 
For the main file ("9517Project.ipynb"), just make sure there is a dataset folder(also contains folders K-01, K-03, V-01, V-02, V-03. However, the folder can contain only some of the data but not all of it(not too few)) in the same directory with a certain number of images and labels.

Contents

	1.	Main Code
	•	The complete source code is in file "9517Project.ipynb".

	2.	Testing Code
	•	"test_on_deeplab.ipynb": Loads the Deeplab model locally, tests its performance on the test dataset, and provides the IoU for each class and the overall mIoU.
	•	"test_on_segformer.ipynb": Loads the Segformer model locally, tests its performance on the test dataset, and provides the IoU for each class and the overall mIoU.

	3.	Visualization Code
	•	"plot_distribution.ipynb": Defines the function to plot the distribution of the labels in our dataset. It loads a CSV file locally, so ensure the CSV file is in the same directory as the code. (If you want to run the test code, copy the corresponding csv file out of the folder and put it under the same file as code.)

	4.	CSV Files
	•	"paths.csv": Contains the file paths of the labels and images in the dataset.
	•	"paths_with_labels.csv": Labels all the images in our dataset.
	•	"sampled_data.csv": Extracts 50% of the data from paths_with_labels.csv.
	•	"train.csv", "val.csv", "test.csv": Generated from sampled_data.csv, representing 70%, 25%, and 5% of the dataset, respectively.
	•	Dataset split: Train size: 3287, Validation size: 1139, Test size: 227.

	5.	Model Files
	•	"SegformerB0.pth" is submitted. Due to file size limitations, DeeplabV3.pth is available for download via the link below.

	6.	Functions
	•	"plot_label_counts()": Plots the distribution of the labels in the dataset.
	•	"calculate_iou()": Calculates the IoU.
	•	"visualize_predictions()": Visualizes the first 5 images in the test dataset and calculates the overall mIoU.
	•	"plot_iou_table()": Displays a table with the IoU for each class in the test data.

	7.	Model Definitions
	•	The first model is defined in the class DeepLabv3(nn.Module).
	•	The second model is defined in the class SegFormerB0(nn.Module).

	8.	Model Testing
	•	As mentioned in points 2 and 3.

	9.	Contact
	•	If you have any concerns, please email us for further information.

	10.	Google Drive Link
	•	https://drive.google.com/drive/folders/1TLwBfvk80gr6RiKKhnTMsK5X8LobFjKK?usp=sharing