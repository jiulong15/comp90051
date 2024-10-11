The code are mainly build based on the logics of machine learning

github link: https://github.com/jiulong15/comp90051.git

## Firstly: Patient Labeling
Identify and labeled the patients based on problem statment in the file patient_label.ipynb

## Secondly： Waveform-decoing
Using waveform_decode.ipynb to decode the waveform data from base64 XML file into numeric data.
the waveform_decode.ipynb are stored in the waveform_preprocessing folder. Store the error messge in folder error list. Manully correct files based on the error list.

## Thirdly: Feature extraction

   In the folder: feature extraction. 
 
   Using waveFeature_extraction.ipynb to extract frequency-based features from every decoded data and concat the results from each data shards.

   Using feature_extraction_part1.ipynb to extract common features such as patients' gender, sex, risk class.

   Then, using feature_extraction_part2.ipynb to extract features based on journal's conclusion about which features have correlation to heart issues, and merge the outputs from other feature extraction.ipynbs to formalize the final training_data.

## Forthly: EDA
   In the folder Model Building, using EDA.ipynb to explore any correlation between data

## Finally: Modeling Building
   Build logistic regression model in LogicRegression.ipynb

   Build SVM model in SVM.ipynb

   Build TabNet model in Tabnet.ipynb






