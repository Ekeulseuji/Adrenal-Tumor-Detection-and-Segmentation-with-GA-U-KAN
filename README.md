# Adrenal-Tumor-Detection-and-Segmentation-with-GA-U-KAN
Not working ah, someone please help me


## **Adrenal Tumor Detection and Segmentation with GA-U-KAN**   

### **1 - Image Format Conversion and Visualization**

- 0.0 Download Abdominal CT scans of kidneys with adrenal lesions with corresponding segmentation labels from the NIH Cancer Imaging Archive https://www.cancerimagingarchive.net/collection/adrenal-acc-ki67-seg/

- 1.0 Load the metadata of the orginal CT scans of kidneys with adrenal lesions, `../DICOM_Files/metadata.csv`

- 1.1 Convert all .DICOM stacks downloaded from NIH Cancer Imaging Archive into .NIfTI format in `../NIFTI_Files/..` for future use

- 1.2 Visualize the `Adrenal_Ki67_Seg_001` CT scan sample and its segmentation result
  

### **2 - Data Split**

- 2.1 Data preprocess, save images of the original scans and their corresponding masks in array form into `images` and `masks` 

- 2.2 Split the porcessed data into `train_input`, `train_label`, `test_input`, and `test_label`
  

### **3 - Finding the Best-performing U-KAN Model Structure**

- 3.1 Define operators used to implement the genetic algorithm (GA), include `Selection`, `Crossover`, `Mutation`

- 3.2 Define the U-KAN model (encoder, bottleneck, decoder) which uses Kolmogorov-Arnold Network Blocks as the bottleneck structure

- 3.3 Define the model loss function `model_loss` = `ce_loss` + `dice_loss` + `regularization_loss`

- 3.4 Use `PatchEmbed` to segment input (training/validation) images into patches and find the best U-KAN model
  

### **4 - Brain Not Braining, Studying Not Studying**
