# Classification and Calibration of Dysarthric Speech

## Introduction
This project aims to classify whether a person has a hearing + neurological disorder or a speech + neurological disorder using Log Mel-Spectrograms of speech data and Convolutional Neural Networks (CNNs).

## Social Background
- According to recent reports from the Korean Society of Laryngeal and Voice Medicine, the number of patients with voice disorders, particularly those over 60, has increased significantly over the past decade. Early diagnosis of speech disorders, including neurological and hearing impairments, can reduce medical costs and improve treatment outcomes.
- Dysarthria, often caused by neurological disorders such as brain tumors, can lead to speech, memory, and cognitive impairments, highlighting the importance of early detection.

## Technical Background
- Traditionally, diagnosing dysarthria relied on subjective auditory perception by clinicians. However, these diagnoses can be influenced by the clinician's skill, experience, and rapport with the patient, leading to inconsistent results.
- To address these issues, we utilize CNN models to analyze dysarthric speech data with higher accuracy, building on previous research (Ha Changjin, Go Taesik, 2023), which used log-mel spectrograms to predict causes of dysarthria.

## Dataset
We used dysarthric speech data from AI Hub (https://www.aihub.or.kr/), consisting of over 5,000 hours of speech data from 1,200 individuals. This dataset can be used for monitoring progress during speech therapy and comparing various intervention methods.

### Data Details
- The dataset includes speech data in the form of wav files along with corresponding metadata in json format, containing:
  - ID, age, gender, region, sampling rate, start/end position, playback time, and file size.
  
  ![img](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/1a581a17-8d5c-4ef2-b393-5aeec3fba967)

## Data Preprocessing
The speech data was processed into log-mel spectrograms to serve as input for the CNN model. Data preprocessing steps included handling variability in pronunciation and ensuring the consistency of spectrogram dimensions.

  ![Preprocessing Image](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/87aea8c5-38c0-41f6-a4fd-2644240ecb72)

## Model Development
- **Model Architecture**: We implemented a CNN architecture for classification, with input features being the log-mel spectrograms of speech data.
- **Training**: The model was trained using the preprocessed data, with hyperparameter tuning to optimize performance.
  
  ![Training Image](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/7d20d9b9-95e5-41d5-aa78-4e16743c12a3)

## Results
- The trained CNN model successfully classified the speech data into hearing + neurological and speech + neurological disorder categories, achieving high accuracy in detecting dysarthric speech patterns.

## Conclusion
This project demonstrates the potential of deep learning models, particularly CNNs, to improve the diagnosis of dysarthric speech disorders using speech data. By automating and improving the accuracy of dysarthria classification, the model supports early detection and better treatment outcomes for patients with speech-related neurological disorders.
