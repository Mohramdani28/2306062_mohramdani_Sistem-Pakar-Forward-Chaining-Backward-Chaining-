APA ITU SISTEM PAKAR?
Sistem Pakar adalah sistem berbasis komputer yang meniru kemampuan pengambilan keputusan seorang pakar dalam bidang tertentu.
Sistem ini menggunakan:

Basis Pengetahuan (Knowledge Base): Kumpulan fakta dan aturan.

Mesin Inferensi (Inference Engine): Mekanisme penalaran (reasoning), yaitu Forward Chaining atau Backward Chaining.

🔁 Forward Chaining (Penelusuran Maju)
📌 Pengertian:
Metode penalaran dari fakta (data) ke arah kesimpulan (tujuan).

🔍 Cara Kerja:
Sistem mulai dari fakta-fakta yang diketahui (input gejala).

Aturan-aturan (rules) yang cocok dengan fakta dipilih.

Fakta baru diturunkan sampai ditemukan kesimpulan/diagnosis.

🎯 Cocok digunakan ketika:
Semua gejala sudah diketahui.

Ingin tahu apa diagnosis/solusinya.

🧪 Contoh Praktikum:
python
Salin
Edit
@Rule(Fact(fever=True) & Fact(cough=True))
def flu(self):
    print("Diagnosis: You may have the flu.")
Jika input: fever=True, cough=True, maka sistem otomatis menyimpulkan flu.

🔙 Backward Chaining (Penelusuran Mundur)
📌 Pengertian:
Metode penalaran dari tujuan (hipotesis) ke arah fakta pendukung.

🔍 Cara Kerja:
Sistem mulai dari dugaan kesimpulan (misalnya: apakah ini flu?).

Sistem bertanya balik kepada pengguna: "Apakah kamu demam?", "Batuk?" dll.

Jika semua syarat terpenuhi, kesimpulan tersebut dianggap benar.

🎯 Cocok digunakan ketika:
Ada tujuan yang ingin dibuktikan.

Sistem menelusuri apakah bukti mendukung diagnosis tersebut.

🧪 Contoh Praktikum:
Sistem ingin tahu apakah pasien flu → lalu menelusuri apakah fever=True, cough=True, dst.

📘 Perbedaan Singkat

Aspek	Forward Chaining	Backward Chaining
Arah Penalaran	Dari data ke kesimpulan	Dari kesimpulan ke data
Pertanyaan diajukan	Di awal (mengumpulkan fakta)	Bertanya sesuai dugaan/hipotesis
Cocok untuk	Diagnosis otomatis berbasis gejala	Pembuktian dugaan tertentu
💡 Kesimpulan Praktikum
Forward Chaining banyak dipakai di sistem pakar diagnosis (misal: penyakit, kerusakan mesin).

Backward Chaining cocok untuk sistem tanya-jawab berbasis hipotesis.

Keduanya penting dipahami dalam praktikum kecerdasan buatan, khususnya di topik sistem pakar berbasis rule-based reasoning.

Kalau kamu butuh contoh kode Backward Chaining atau contoh implementasi lainnya (GUI, web, atau logika hybrid), tinggal bilang aja!
