# hse_hw2_chip
[Google Colab](https://colab.research.google.com/drive/1-HsGZ5naq_dXZ7L61bdX1MlkpC-5nYU3?usp=sharing)
### FastQC
>Не делалось подрезание файлов, так как в основном все параметры были в норме, однако качество **Per Sequence GC Content**, **Per base sequence content** было не совсем идеальным.

##### ENCFF001QWW – Total Sequences: 21099652
<img width="800" alt="Screen Shot 2022-03-10 at 22 19 19" src="https://user-images.githubusercontent.com/55647212/157738643-9df3f9ea-708b-47f8-807e-e52c60936030.png">
<img width="800" alt="Screen Shot 2022-03-10 at 22 19 39" src="https://user-images.githubusercontent.com/55647212/157738794-4c55702e-b412-473a-b97a-6df3a362e1ce.png">
<img width="800" alt="Screen Shot 2022-03-10 at 22 19 31" src="https://user-images.githubusercontent.com/55647212/157738719-cee325a4-3d7d-4421-82c9-7d78b1edd4ee.png">

##### ENCFF001QWX – Total Sequences: 46226003
<img width="800" alt="Screen Shot 2022-03-10 at 22 22 16" src="https://user-images.githubusercontent.com/55647212/157738953-f9c18034-09fc-49af-b3ce-b39a1a0f16a1.png">

##### ENCFF283HQV
<img width="800" alt="Screen Shot 2022-03-10 at 22 23 24" src="https://user-images.githubusercontent.com/55647212/157739273-07fba5bd-eeac-42b7-9b86-dad00667099f.png">
<img width="800" alt="Screen Shot 2022-03-10 at 22 23 31" src="https://user-images.githubusercontent.com/55647212/157739510-7e41d902-3a5f-42b7-a227-5d022f261c9e.png">
<img width="800" alt="Screen Shot 2022-03-10 at 22 23 43" src="https://user-images.githubusercontent.com/55647212/157739527-f1d33759-9281-485f-ac91-99a11dced1c6.png">

### Data statistics
**ID** | **All reads** | **Uniqie (%)** | **Not Uniqie** | **Misaligned** 
------------ | ------------- | ------------- | ------------- | ------------- 
ENCFF001QWW	| 21099652 | 1037673 (4.92%) | 3142269 (14.89%) | 16919710 (80.19%)
ENCFF001QWX | 46226003 | 2211574 (4.78%) | 7061963 (15.28%) | 36952466 (79.94%)
ENCFF283HQV | 10424077 | 546743 (5.25%) | 1349469 (12.95%) | 8527865 (81.81%)

>Почему процент выравниваний получился именно таким?

Так как картирование на 1 хромосому, в коротких последовательностях (в нашем случае это 1 хромосома) повышается процент повторений, что выявило низкий уровень уникальных ридов

### Venn Diagrams
> Проанализируйте полученные результаты и приведите свои рассуждения в README.md.

Во втором случае получилось намного меньше shared peaks, может быть, это вызвано тем, что 2 чтение в 2 раза больше первого, получилось больше совпадений. 
> Как можно объяснить различия в количестве пересечений?

Сначала мы накладываем пики из 1 файла на пики из 2 и наоборот: то есть в первый раз мы берем пики из 1 файла и смотрим, что есть из 1 во втором, а во 2 раз наоборот. 

### NGS Plot
<img width="400" src="https://user-images.githubusercontent.com/55647212/157757980-10e2ca0c-9d04-4cb0-8443-7bc8ba3cefb5.png">

Данные из ENCODE согласуются с данными *Li e. al. (2007) Cell*: сначала наблюдается резкое снижение количества гистоновых меток (inactive), но после TSS мы видим резкое увеличение гистоновых меток (active).

