# MI_ALPR
Automatic License Plate Recognition (ALPR) Code trained on Michigan and International License Plates; using YOLOv8, EasyOCR, Google Colab.

## Research Paper
This ALPR implementation is based off a research paper, *Evaluation of Domestic and Internationally Trained YOLO License Plate Recognition Models*, which I completed for a high school AP Research class and am in the process of continuing and publishing. Read the *[full research paper here](https://drive.google.com/file/d/1kUmTvX3GqSsCtqUI_huuLBuLk2l5zccI/view?usp=sharing)*. If this is helpful at all to your research please cite the linked paper.

## Goal
The goal of this research is to determine whether a YOLO/OCR ALPR implementation is more accurate (when tested on Michigan license plates), when its YOLO model is trained solely on license plates from the state of interest (Michigan), or trained solely on international license plates. 

## Important Credits
The international license plates for this project were obtained from:
- OpenALPR Benchmark Set |  *European Union and Brazil*  |  *[link](https://github.com/openalpr/openalpr)*
- Chinese City Parking Dataset (CCPD) | *China*
  - Xu, Z., Yang, W., Meng, A., Lu, N., Huang, H., Ying, C., & Huang, L. (2018). Towards End-to-End License Plate Detection and Recognition: A Large Dataset and Baseline.
- Application Oriented License Plates (AOLP) | Taiwan
  - Hsu, G.-S., Chen, J.-C., & Chung, Y.-Z. (2013). Application-Oriented License Plate Recognition. IEEE Transactions on Vehicular Technology, 62(2), 552–561.
- UFPR-ALPR | Brazil
  - Laroca, R., Severo, E., Zanlorensi, L. A., Oliveira, L. S., Gonçalves, G. R., Schwartz, W. R., & Menotti, D. (2018, July 1). A Robust Real-Time Automatic License Plate Recognition Based on the YOLO Detector. IEEE Xplore.
- Vehicle-Rear | Brazil
  - De, O., Rayson Laroca, Menotti, D., Veronica, K., & Minetto, R. (2021). Vehicle-Rear: A New Dataset to Explore Feature Fusion for Vehicle Identification Using Convolutional Neural Networks. IEEE Access, 9, 101065–101077.

**If you use any of the international images from this project in yours, be sure to credit the original source!**

## Results and Future Work

The YOLOv8 model trained very well, however final detection in the combined YOLO/OCR algorithm was poor, with 12% recognition in the combined model.

<img width=fit height="200" alt="image" src="https://github.com/user-attachments/assets/f4d3fb9c-6184-4996-bf84-f086c64381f4" />  <br><br>

#### <ins>Possible reasons for difference between detection and recognition accuracy:</ins>
- Low number of training images (~270 for each the International and Domestic models)
- Poor image localization, especially with extraneous license plate characters
  - These include the state name (Michigan), and especially license plate frames being read as part of the license plate.
- Similar characters being confused for each other:
  - Z, 1, and 7
  - S and 5
  - W and X
  - N and H
  - 6, G, and E
  - K and X
  - O, Q, and 0
  - 8 and 0
  - I and 1
 
  - This can be fixed reliatively easily in the next iteration because there are characters (such as the letter O and special characters) which do not appear on Michigan license plates. The algorithm can automatically replace any "false" characters with their "real" counterparts.
 
- Possible problems with image quality and image pipeline settings in the code.


#### Contact? Questions?
Email jgtewo2025@ gmail.com
