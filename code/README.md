The code are mainly build based on the logics of machine learning


Firstly, Identify and labeled the patients based on problem statment in the file patient_label.ipynb

Secondly, Using waveform_decode.ipynb to decode the waveform data from base64 XML file into numeric data.
   the waveform_decode.ipynb are stored in the waveform_preprocessing folder. Store the error messge in folder error list. Manully correct files based on the error list.

Thirdly, In the folder: feature extraction. Using waveFeature_extraction.ipynb to extract frequency-based features from every decoded data and concat the results from each data shards.

Forthly, In the folder: feature extraction. Using feature_extraction_part1.ipynb to extract common features such as patients' gender, sex, risk class.

Fifthly, In the folder: feature extraction. Using feature_extraction_part2.ipynb to extract features based on journal's conclusion about which features have correlation to heart issues, and merge the output from other feature extraction.ipynb to formalize the train_data.




