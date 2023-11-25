# SkimLit (Advance NLP Model using Deep Learning) 💻🔥

SkimLit merupakan proyek dalam bidang Natural Language Processing (NLP) yang bertujuan untuk membantu dalam penandaan dan pencarian informasi penting dalam dokumen abstrak publikasi medis. Proyek ini menggunakan teknik-teknik NLP untuk membuat model yang mampu menyoroti dan menandai bagian-bagian penting dalam abstrak dari publikasi ilmiah. Dataset yang digunakan dalam proyek ini adalah RCT Pubmed, yang terdiri dari abstrak dari berbagai penelitian klinis acak (RCT) yang dipublikasikan di PubMed.

## Dataset 

Proyek ini menggunakan dataset RCT Pubmed yang berisi abstrak dari penelitian klinis acak yang diterbitkan di PubMed. Dataset ini dapat diakses melalui [Dataset RCT Pubmed](https://github.com/Franck-Dernoncourt/pubmed-rct). 

Didalamnya terdapat 4 dataset yang berbeda-beda yaitu :
* **PubMed_200k_RCT** : Dataset ini memiliki ~200.000 labelled Randomized Controlled Trial (RCT) abstrak .
* **PubMed_200k_RCT_numbers_replaced_with_at_sign** : Dataset ini juga memiliki ~200.000 labelled Randomized Controlled Trial (RCT) abstrak namun semua angka didalamnya diganti dengan simbol '@'.
* **PubMed_20k_RCT** : Dataset ini memiliki ~20.000 labelled Randomized Controlled Trial (RCT) abstrak .
* **PubMed_20k_RCT_numbers_replaced_with_at_sign** : Dataset ini juga memiliki ~20.000 labelled Randomized Controlled Trial (RCT) abstrak namun semua angka didalamnya diganti dengan simbol '@'.

## Algoritm For This Project
* Mengunduh dataset teks ([PubMed RCT20k dari GitHub](https://github.com/Franck-Dernoncourt/pubmed-rct))
* Menulis fungsi preprocessing untuk mempersiapkan data kita untuk pemodelan
* Menyiapkan serangkaian percobaan pemodelan
  * Membuat Pipeline (TF-IDF Classifier)
  * Membuat Deep Learning model combinations of: token embeddings
* Membangun model multimodal pertama kami (mengambil beberapa jenis input data)
  * Mereplikasi arsitektur model dari https://arxiv.org/abs/1612.05251
* Menemukan prediksi yang paling salah
* Membuat prediksi pada abstrak PubMed. 

## Machine Learning Model 
* **NaiveBiase Model** (sklearn) 
![Model_0](https://media.discordapp.net/attachments/715823338655580171/1178049168909021205/image.png?ex=6574bac8&is=656245c8&hm=a01024d450e607792715e018c6fa40e0041fe2b4a75546ef4f14f30826261a20&=&format=webp&width=717&height=341)
<br>
Accuracy of this model -> **72%**

* **Conv1D Model** (TensorFlow) 
![Model_1](https://media.discordapp.net/attachments/715823338655580171/1178049244859469976/image.png?ex=6574badb&is=656245db&hm=eab5bb8307fad01218967e781656493dcbd73087536354a4ddb19c4a5245db5c&=&format=webp&width=717&height=189)
<br>
Accuracy of this model -> **78%**

## Exercise and Extras

<div align="center" style="font-weight: bold; font-size: 25px">Steps in modeling with TensorFlow</div>

<div align="center">
    <img src="https://media.discordapp.net/attachments/715823338655580171/1178053283848392795/misc-tensorflow-workflow-outline.png?ex=6574be9e&is=6562499e&hm=2ba5876b920126c4bfffc11f9f63e65e4e70510ac80a5539934812b414b7ec96&=&format=webp&width=717&height=174">
</div>

1. Coba pahami TensorFlow Workflow diatas.
2. Coba melatih `model_1` dengan epochs yang banyak hingga model mendapatkan akurasi yang tinggi namun tidak mengalami overfitting.
3. Coba mainkan komponen train pada `model_1` seperti optimization function atau activation function hingga mendapatkan model akurasi yang cukup tinggi.
4. Coba dengan dataset yang lebih tinggi lagi seperti 200k RCT.

## Colaborators
1. [Maulana Al Iqbal Widodo_L200210136](https://github.com/Abstrakx)
2. [Muhammad Dzaki Hanifa_L200210032](https://github.com/Dzakihanifa12)
3. [Alif Rahmat Yudha Putra_L200210198]()
4. [Zildan Alfatih Agustian_L200210109]()