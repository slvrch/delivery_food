# Background Project
SwiftBite Delivery menghadapi tantangan dalam menjaga kecepatan dan efisiensi delivery di tengah tingginya volume order serta kondisi lalu lintas yang dinamis. Rata-rata delivery duration mencapai 26.29 menit dengan 22.85% order termasuk kategori High Risk, yang menunjukkan masih tingginya kompleksitas operasional delivery.
Traffic congestion, peak hour, workload delivery dan kompleksitas jarak pengiriman berkontribusi terhadap bottleneck operasional yang berdampak pada keterlambatan delivery dan efisiensi operasional.
Project ini bertujuan membangun dashboard monitoring operasional untuk membantu tim operasional memonitor traffic bottleneck, operational risk, delivery performance dan efisiensi delivery.

# Business Problem

- Identifikasi kondisi operasional yang berkontribusi terhadap peningkatan delivery duration dan bottleneck delivery
- Monitoring distribusi operational risk berdasarkan kondisi
traffic, workload delivery, dan pola operasional delivery
- Evaluasi efisiensi delivery berdasarkan jarak pengiriman dan dampaknya terhadap delivery performance

# Analytical Questions

- Kondisi traffic mana yang menghasilkan delivery duration tertinggi?
- Kapan bottleneck delivery paling sering terjadi?
- Apakah workload delivery meningkatkan delivery delay?
- Kategori operational risk mana yang memiliki delivery duration tertinggi?
- Area mana yang memiliki proporsi High Risk terbesar?
- Kapan High Risk order paling sering muncul?
- Apakah delivery distance mempengaruhi delivery duration?
- Kategori jarak delivery mana yang memiliki operational risk tertinggi?

# Data Understanding

Dataset Source: Zomato Delivery Operations Analytics
Dataset Overview: 45.584 data order delivery dan 20 fitur operational delivery pada periode tahun 2022
Kategori Fitur: 

- Traffic & lingkungan operasional
- Operasional delivery
- Geolokasi
- Fitur berbasis waktu

Data Quality Issues:

- Missing values pada fitur operasional
- Format data waktu tidak konsisten
- Data koordinat tidak valid
- Anomali jarak delivery

Operational Traffic ipynb: https://colab.research.google.com/drive/1l0wYaYomI8yJRKDRwwljY2EUCDQIiTrL?usp=sharing

# Operational Risk Scoring

Menentukan beberapa faktor operasional yaitu, kepadatan traffic, multiple deliveries, kondisi peak hour, delivery distance, durasi pickup delay, dan kondisi cuaca.
Selanjutnya, setiap fitur diberikan score 1-3 berdasarkan besar pengaruh pada hambatan operasional pengiriman lalu score setiap baris dijumlahkan dengan total score termasuk kategori risk operational seperti Low Risk, Medium Risk, dan High Risk yang rentang score risk dari nilai minimum, median dan maksimum.

# Analysis
Traffic Bottleneck Analysis

<img width="1123" height="239" alt="image" src="https://github.com/user-attachments/assets/694c3731-9e38-4542-8d1e-d71afdfd7074" />

Insight:
- Jam traffic menghasilkan delivery duration tertinggi dan duration delivery meningkat seiring kenaikan traffic density
- Bottleneck delivery paling sering terjadi saat dinner period
- Multiple deliveries meningkatkan delivery duration dan memperparah operational bottleneck

High-Risk Delivery

<img width="1199" height="267" alt="image" src="https://github.com/user-attachments/assets/f8fdd8e7-0c05-4c89-a65c-4ff452e54f38" />

Insight:
- High risk memiliki rata-rata delivery duration tertinggi
- High risk operational paling sering terjadi saat dinner peak congestion **~54%**
- Semi-Urban area memiliki proporsi High Risk order terbesar **~72%**

Delivery Distance & Operational Risk

<img width="1309" height="348" alt="image" src="https://github.com/user-attachments/assets/2e19511a-2dfa-4f3b-97b3-24d17b57fe65" />

Insight:
- Long distance delivery memiliki average delivery duration tertinggi
- Operational risk meningkat seiring bertambahnya delivery distance, dengan long-distance operations memiliki proporsi High Risk tertinggi **~40%**

# Recommendation

- Mengoptimalkan workload delivery untuk mengurangi operational overload 
- Memprioritaskan monitoring operasional pada area Semi-Urban untuk mengurangi konsentrasi High-Risk delivery
- Menerapkan route optimization pada long-distance delivery untuk meningkatkan efisiensi pengiriman
