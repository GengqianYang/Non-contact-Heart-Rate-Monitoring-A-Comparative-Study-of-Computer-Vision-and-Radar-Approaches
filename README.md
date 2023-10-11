# Non-contact Heart Rate Monitoring: A Comparative Study of Computer Vision and Radar Approaches
Gengqian Yang, Benjamin Metcalfe, Robert Watson, and Adrian Evans
## Introduction
The Heart Rate (HR) is a vital sign that is used to assess the physical and mental state of an individual. There is a growing interest in incorporating HR measurement into Driver Monitoring Systems (DMS), providing physiological measurements to help address long-existing road safety issues by minimising human error. In real-world driving scenarios, the HR must be measured using non-contact approaches that avoid distracting or restricting the driver. The most common approaches to non-contact HR measurement use either computer vision (CV) or mm-wave radar, both showing acceptable performances in controlled studies. However, the relative merits of different sensor modalities for real-world scenarios remain unclear, and the potential benefits of a combined approach are unquantified. To address these questions, this paper first proposes and implements non-contact HR measurement architectures for both CV and mm-wave radar systems and characterises their HR estimation performance, using electrocardiography (ECG) to provide ground truth measurements. The effects of distance to sensors and of illumination variations on HR estimation are also studied, showing the relative errors for both modalities to be less than 0.5% for the distances found in practical DMS. These results also highlight the distinctive characteristics of each modality and the benefits of a multi-modality approach for DMS.
## Prerequisites
Python 3;
OpenCV python;
Deepface;
ltr11 (for the bgt60ltr11aip radar);
pyrealsense2 (for the realsense RGBD camera).
## Proposed CV-based HR Monitoring Architecture
![image](https://github.com/GengqianYang/Dataset/assets/62884839/41f4d109-e610-4efb-93f4-e29ff4812b41)
## Proposed Radar-based HR Monitoring Architecture
![image](https://github.com/GengqianYang/Dataset/assets/62884839/c3b88026-6853-404b-b28a-0b852a00e4f5)
## Variation of IBI Distribution with Sensor Modality
Due to the different underlying principles of the ECG and non-contact HR monitoring methods, there are variations in the IBI distributions obtained from each sensor type. For example, the ECG measures electrical activity so the timing of the peak with the highest amplitude (the R-peak) does not exactly coincide with the resulting cardiac muscle contraction, and the peaks in radar signals are related to mechanical changes occurring sometime after the muscle contraction. For the CV-based rPPG method, the detected peaks lag the ECG due to the time taken for the blood volume to change.
![image](https://github.com/GengqianYang/Dataset/assets/62884839/72141916-4e4a-4292-9b30-ffd0bda14746)![image](https://github.com/GengqianYang/Dataset/assets/62884839/0b73c386-4af0-4a55-ab77-7e0268de9270)
![image](https://github.com/GengqianYang/Dataset/assets/62884839/b1cefa52-2f71-4899-8df6-2952e2a6699e)![image](https://github.com/GengqianYang/Dataset/assets/62884839/0b205670-98ad-44c7-82bb-ec4e96a176d6)






