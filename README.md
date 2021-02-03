# People Analytics: Best Performance Employee in One Year Ahead

This is a project I am working on during the BRI Hackathon 2021 competition meanwhile I'm in a free time together with applying a jobs related to data science field. The goal of this project is to classify the employee performance based on 2 aspect which is best performance (1) and not best (0). In order to accomplish the business goal, I apply some machine learning model using ROC-AUC metrics. The model performance was quite good and need further improvement especially on the data balance. In addition, it can be summarized that the amount of employee who dont achieve best performance is more high compared to who achieve best performance.

# Data 

I am using the BRI Hackathon 2021 : People Analytic data found in Kaggle. The dataset contains the following features:
* job_level : Level Jabatan Pekerja
* job_duration_in_current_job_level : Masa Kerja pada job level saat ini
* person_level : Level personal Pekerja
* job_duration_in_current_person_level : Masa Kerja pada person level saat ini
* job_duration_in_current_branch : Masa Kerja pada unit kerja saat ini
* Employee_type : Tipe Pekerja ( 3 tipe Relationship Manager, tipe A, B , dan C)
* gender : Jenis Kelamin
* age : Usia
* marital_status_maried(Y/N) : Status Pernikahan (Y / N)
* number_of_dependences : Jumlah anak dalam tanggungan
* Education_level : Tingkat pendidikan
* GPA : IPK
* year_graduated : Tahun lulus
* job_duration_from_training : lama bekerja mulai dari training
* branch_rotation : Jumlah rotasi pindah unit kerja
* job_rotation : jumlah rotasi pindah jabatan
* assign_of_otherposition : jumlah rotasi penugasan
* annual leave : jumlah cuti tahunan
* sick_leaves : jumlah izin sakit
* Last_achievement_% : presentase pencapaian triwulan terakhir terhadap target
* Achievement_above_100%_during3quartal : Jumlah pencapaian diatas 100% dalam 3 tahun terkahir
* Best Performance : Termasuk dalam best performance (1/0)


# Model 

Due to imbalanced data, I'm building two models, one using StratifiedKFold sampling with LGBM model and the other one using SMOTEENN resampling with Random Forest Classifier model. Figure below shows the data imbalance before performing data balancing technique. 

<p align="center">
  <img src="https://github.com/dmsardhty/People-Analytic/blob/master/1.png" />
</p>

For the first model, I try to use StratifiedKFold splitting to handle the data imbalance according to the literature and some blog contents that i read. After that i perform an LGBM Classifier model with 3 data split consists of train, validation, and test. The results show that after 5 folding, a 0.7 AUC scores is generated in training set and turns to 0.6 AUC scores on validation set. The following AUC curve for this model are as shown below:

<p align="center">
  <img src="https://github.com/dmsardhty/People-Analytic/blob/master/3.png" />
</p>

Feels cognizant about the unsatisfying model performance, I intend to use another resampling method using SMOTEENN and turns out like this:

<p align="center">
  <img src="https://github.com/dmsardhty/People-Analytic/blob/master/2.png" />
</p>

Furthermore, I add the Random Forest model with RandomizedSearchCV tuning and obtained a quite good score on validation which is **0.96 AUC score**.

# Feature Importance 

<p align="center">
  <img src="https://github.com/dmsardhty/People-Analytic/blob/master/4.png" />
</p>


