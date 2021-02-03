# People Analytics: Best Performance Employee in One Year Ahead

This is a project I am working on during the BRI Hackathon 2021 competition meanwhile I'm in a free time together with applying a jobs related to data science field. The goal of this project is to classify the employee performance based on 2 aspect which is best performance (1) and not best (0). In order to accomplish the business goal, I apply some machine learning model using ROC-AUC metrics. The model performance was quite good and need further improvement especially on the data balance. In addition, it can be summarized that the amount of employee who dont achieve best performance is more high compared to who achieve best performance.

# Data 

I am using the BRI Hackathon 2021 : People Analytic data found in Kaggle. The dataset contains the following features:
job_level : Level Jabatan Pekerja
job_duration_in_current_job_level : Masa Kerja pada job level saat ini
person_level : Level personal Pekerja
job_duration_in_current_person_level : Masa Kerja pada person level saat ini
job_duration_in_current_branch : Masa Kerja pada unit kerja saat ini
Employee_type : Tipe Pekerja ( 3 tipe Relationship Manager, tipe A, B , dan C)
gender : Jenis Kelamin
age : Usia
marital_status_maried(Y/N) : Status Pernikahan (Y / N)
number_of_dependences : Jumlah anak dalam tanggungan
Education_level : Tingkat pendidikan
GPA : IPK
year_graduated : Tahun lulus
job_duration_from_training : lama bekerja mulai dari training
branch_rotation : Jumlah rotasi pindah unit kerja
job_rotation : jumlah rotasi pindah jabatan
assign_of_otherposition : jumlah rotasi penugasan
annual leave : jumlah cuti tahunan
sick_leaves : jumlah izin sakit
Last_achievement_% : presentase pencapaian triwulan terakhir terhadap target
Achievement_above_100%_during3quartal : Jumlah pencapaian diatas 100% dalam 3 tahun terkahir
Best Performance : Termasuk dalam best performance (1/0)
