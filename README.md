# BisualLabDMR cleaned images

This repository includes preprocessed and segmented breast thermography images derived from the Database for Mastology Research with Infrared Image (DMR-IR), originally captured at Antonio Pedro University Hospital. Only sequences acquired under the Dynamic Infrared Thermography (DIT) protocol were used. These images were obtained using a FLIR SC-620 IR camera with a resolution of 640×480 pixels, and a thermal stimulus was applied during acquisition to enhance vascular responses.

The following preprocessing steps were applied:

Data Cleansing: Patients with fewer than 20 sequential frames, blurry images, or occlusions (e.g., bandages or implants) were excluded.

ROI Segmentation: A fully automated segmentation process was conducted using a U-Net model trained on 40 manually segmented frames. The segmentation was designed to isolate the breast region and exclude unrelated anatomical structures such as the neck and abdomen.

Normalization: Images were normalized using pixel intensity scaling (min–max normalization) and resized to 224×224 pixels.

Selection Criteria: Only patients with complete and usable sequences were retained, ensuring consistency across samples.

If you use this dataset, please cite the DMR-IR database as follows:

Silva, L. F.; Saade, D. C. M.; Sequeiros, G. O.; Silva, A. C.; Paiva, A. C.; Bravo, R. S.; Conci, A.
A New Database for Breast Research with Infrared Image. Journal of Medical Imaging and Health Informatics, Vol. 4, No. 1, March 2014, pp. 92–100.
DOI: 10.1166/jmihi.2014.1236

If you are interested in the full methodology used for preprocessing, segmentation, and classification of these images, please refer to:

Munguía-Siu, A.; Vergara, I.; Espinoza-Rodríguez, J.H. (2024).
The Use of Hybrid CNN-RNN Deep Learning Models to Discriminate Tumor Tissue in Dynamic Breast Thermography.
Journal of Imaging, 10(12), 329. https://doi.org/10.3390/jimaging10120329
