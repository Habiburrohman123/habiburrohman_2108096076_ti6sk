**Penjelasan Program**
from gpio import * dan from time import *
	Mengimpor fungsi-fungsi yang diperlukan dari library GPIO dan modul time.
def sensorGerakan()
	Ini adalah fungsi yang digunakan untuk membaca input dari sensor gerak yang terhubung ke pin GPIO. Fungsi ini akan menampilkan pesan "tidak ada gerakan" jika sensor tidak mendeteksi gerakan, dan akan menyalakan dua output kustom (menggunakan fungsi customWrite) jika sensor mendeteksi gerakan.
def main()	
  Ini adalah fungsi utama yang akan dijalankan ketika program dimulai. Di dalam fungsi ini, kita menggunakan add_event_detect(0, sensorGerakan) untuk menambahkan fungsi sensorGerakan sebagai callback yang akan dipanggil ketika perubahan terdeteksi pada pin input (pin 0 dalam contoh ini).
while True: delay(1000)	
  Ini adalah loop utama yang berjalan terus-menerus. Dalam loop ini, kita menggunakan delay(1000) untuk menunda eksekusi program selama 1 detik.
if __name__ == "__main__" : main()	
  Ini adalah bagian yang menjalankan fungsi main() ketika file Python dieksekusi langsung. Ini memastikan bahwa fungsi main() akan dijalankan ketika file Python dieksekusi sebagai skrip, tetapi tidak akan dijalankan jika file tersebut diimpor sebagai modul oleh skrip Python lainnya.
