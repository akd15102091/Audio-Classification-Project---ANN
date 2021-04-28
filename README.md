# Audio-Classification-Project---ANN

Dataset link : https://urbansounddataset.weebly.com/download-urbansound8k.html

About Dataset :
      
      1) There are around 8000+ sounds files with 10 different type of voice (class) .
      
      2) The class name: air_conditioner, car_horn, children_playing, dog_bark, drilling, engine_idling, gun_shot, jackhammer, siren, street_music.
      
      3) One CSV file is also given, in which the columns are : **slice_file_name** , fsID, start, end, salience, **fold, classid, class** .

      4) For project, we will use this csv file and sound files.



We will solve this task using **LIBROSA** library .

------------------------------------------------------------------------------

**1) Exploratory Data Analysis** :

![a1](https://user-images.githubusercontent.com/61588604/116344616-2e984a00-a804-11eb-82e3-a85d65aa8c98.png)

let read another sound file with the help of librosa and scipy.

![a2](https://user-images.githubusercontent.com/61588604/116344934-c4cc7000-a804-11eb-8bac-80087a9b37dc.png)

![a3](https://user-images.githubusercontent.com/61588604/116344939-c6963380-a804-11eb-9991-c15c8fe8b79f.png)


--------------------------------------------------------------------------------

**Differences between librosa and scipy, when read sound file......**
      
      1) Librosa converts the signal to mono, meaning the channel will always be 1. But Scipy can't, means if tehre are two channels in signal then it will kepp both channels.
      
      2) Librosa can represent an audio signal with respect to a normalized pattern (btw -1 to 1),so the regular pattern is observed from all files.  but scipy does not give normalised data .

      3) Librosa by default convert sample rate into 22050 .


----------------------------------------------------------------------------------

**2) Data Preprocessing** :

      a) For data preprocessing, we used MFCC for extracting features.
      
      b) I used Mel-Frequency Cepstral Coefficients(MFCC) from the audio samples. The MFCC summarises the frequency distribution across the window size, so it is possible to analyse both the frequency and time characteristics of the sound. These audio representations will allow us to identify features for classification.

      c) One by one read row and take file from folder and extracted features MFCC using Librosa.






