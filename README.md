# README

## Nama    : Resanda Dezca Asyam

## NPM     : 2206082682

## Kelas   : PBP C


Penjelasan Dari Soal-Soal:
1. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).

    **a.  Membuat sebuah project Django awal**

        Saya memulai proyek pengelolaan inventori game pada karakter LightReborn dengan langkah-langkah yang terstruktur. Pertama-tama, 
        saya memulai dengan menginisiasi repositori baru menggunakan perintah "git init" Ini secara otomatis membuat repositori Git 
        kosong di dalam direktori yang sebelumnya telah saya buat, yaitu "resa_lightreborn." Langkah berikutnya adalah menginisiasi 
        repositori di GitHub untuk memulai pelacakan perubahan proyek "resa_lightreborn" secara daring. Setelah itu, saya menghubungkan 
        repositori lokal dengan repositori di GitHub, memastikan bahwa semua perubahan dapat disimpan secara online.

        Langkah selanjutnya adalah menginstalasi Django dan menginisiasi proyek Django. Untuk menjaga lingkungan yang terisolasi, saya    
        mengaktifkan Virtual Environment di dalam direktori "resa_lightreborn." Setelah itu, saya menyiapkan semua dependensi yang 
        diperlukan dan membuat proyek Django. Selanjutnya, saya melakukan konfigurasi proyek dengan mengizinkan akses dari semua host, 
        memastikan bahwa aplikasi dapat diakses secara luas. Untuk memverifikasi apakah proyek Django berhasil dibuat, saya menjalankan 
        server lokal.Terakhir, saya mengunggah proyek "resa_lightreborn" ke repositori GitHub dengan membuat berkas ".gitignore" untuk 
        menentukan berkas-berkas dan direktori-direktori yang harus dikecualikan oleh Git. Setelah itu, saya menjalankan proses "add," 
        "commit," dan "push" dari direktori repositori lokal, sehingga proyek saya dapat terus berkembang.
        
    **b.  Membuat aplikasi bernama main pada project yang telah dibuat** 

        Selanjutnya, saya menjalankan instruksi "python manage.py startapp main" untuk menciptakan direktori baru yang diberi nama 
        "main." Di dalam direktori ini, saya memulai proses pembangunan struktur awal aplikasi, yang akan digunakan untuk menampilkan 
        informasi inventori karakter pada app lightreborn.    

    **c.  Melakukan routing pada proyek agar dapat menjalankan aplikasi main**

        Setelah berhasil membuat aplikasi "main," langkah selanjutnya adalah mendaftarkannya ke dalam proyek Django agar dapat diakses 
        dan digunakan. Tahap ini melibatkan penambahan 'main' ke dalam daftar aplikasi yang telah terdaftar dalam variabel 
        "INSTALLED_APPS" yang ada di berkas "settings.py". Berkas "settings.py" tersebut terletak di dalam direktori proyek 
        "resa_lightreborn". Setelah itu, saya menciptakan sebuah folder bernama template yang berisi "main.html" dalam direktori 
        "templates" yang telah dibuat sebelumnya dalam  aplikasi "main." Template ini memiliki peran krusial dalam tampilan inventori 
        karakter lightreborn. Dalam proses pembuatan "main.html," saya mengisi template tersebut dengan kode HTML yang sederhana, 
        termasuk elemen-elemen seperti judul(application), nama, dan class. Tujuannya adalah untuk memeriksa tampilan dasar halaman HTML 
        yang akan digunakan untuk menampilkan informasi inventori karakter lightreborn.
    
    **d.  Mulai membuat model pada aplikasi main dengan nama Item dan memiliki atribut wajib seperti pada tugas 2**

        Tahap berikutnya dari project Inventori Karakter LightReborn, saya melakukan beberapa perubahan dalam berkas "models.py" yang 
        terletak dalam direktori aplikasi "main." Perubahan ini dimaksudkan untuk mengintroduksi model baru yang diberi nama "Item." 
        Model ini mengandung beberapa bidang, termasuk "name" untuk menyimpan nama item dengan tipe data CharField, "amount" untuk 
        menyimpan jumlah item dengan tipe data IntegerField, dan "description" untuk menyimpan deskripsi item dengan tipe data TextField, 
        yang memungkinkan penyimpanan teks yang lebih panjang. Setelah model "Item" didefinisikan, langkah berikutnya adalah menciptakan 
        dan menerapkan migrasi model. Ini merupakan langkah kunci dalam melacak perubahan pada model basis data.

    **e.  Membuat sebuah fungsi di views.py yang akan menghasilkan output ke dalam sebuah template HTML. Output tersebut akan menampilkan nama aplikasi dan juga nama serta kelas yang dibuat**
 
        Lalu, saya melanjutkan dengan mengintegrasikan komponen MVT (Model-View-Template) dalam kerangka kerja Django. Pertama, saya 
        mengimpor modul yang diperlukan dan membuat sebuah fungsi view yang dinamakan "show_main". Fungsi "render" yang berasal dari 
        modul "django.shortcuts" digunakan untuk merender tampilan HTML dengan data yang diberikan.

        Fungsi "show_main" menerima parameter "request" yang merupakan objek permintaan HTTP dari pengguna. Fungsi ini berperan dalam 
        mengatur permintaan tersebut dan mengembalikan tampilan yang sesuai. Dalam fungsi "show_main," saya menggunakan dictionary 
        "context" untuk mengemas data yang akan disampaikan ke tampilan. Data yang dimasukkan meliputi nama aplikasi, serta nama dan 
        kelas yang relevan dengan proyek.

        Saya menggunakan fungsi "render" dengan tiga argumen: "request" sebagai objek permintaan HTTP, "main.html" sebagai nama berkas 
        template, dan "context" sebagai dictionary yang berisi data untuk membuat tampilan menjadi dinamis. Selama proses ini, saya juga 
        mengubah judul (nama aplikasi), nama, dan kelas yang sebelumnya statis dalam tampilan HTML menjadi kode Django yang memungkinkan 
        nilai-nilainya berasal dari variabel-variabel yang telah didefinisikan dalam "context".

    **f.  Menyiapkan routing dalam berkas "urls.py" aplikasi "main" untuk mengaitkan fungsi yang telah saya buat dalam "views.py".**

        Pertama-tama, saya melakukan konfigurasi routing URL untuk aplikasi "main" dengan membuat berkas baru yang dinamakan "urls.py" di 
        dalam direktori "main". Fungsi dari berkas "urls.py" ini adalah mengatur bagaimana rute URL terkait langsung dengan aplikasi 
        "main" akan ditangani.

        Selanjutnya, saya melanjutkan dengan mengonfigurasi routing URL pada tingkat proyek secara keseluruhan. Ini dilakukan dengan 
        menambahkan rute URL yang akan mengarahkan pengguna ke tampilan yang ada di aplikasi "main." Rute URL ini kemudian dimasukkan ke 
        dalam variabel "urlpatterns" yang terdapat dalam berkas "urls.py" yang berada di dalam direktori proyek "resa_lightreborn."

        Dengan konfigurasi ini, proyek sekarang memiliki mekanisme yang jelas untuk mengarahkan permintaan URL pengguna ke tampilan yang 
        sesuai dalam aplikasi "main."

    **g.  *Unit Testing*, membuat berkas README.md, dan melakukan proses deployment aplikasi yang sudah dibuat agar dapat diakses oleh teman-teman melalui internet.**

        Pertama-tama, saya telah membuat serangkaian unit testing untuk memverifikasi bahwa kode yang telah saya tulis berfungsi sesuai 
        dengan yang diharapkan. Salah satu pengujian adalah "test_main_url_is_exist," yang berfungsi untuk memeriksa apakah alamat URL 
        "/main/" dapat diakses dengan sukses. Pengujian lainnya adalah "test_main_using_main_template," yang bertujuan untuk memastikan 
        bahwa halaman "/main/" dirender dengan benar menggunakan template "main.html." Terakhir, ada pengujian "test_item_model" yang 
        mengonfirmasi kemampuan aplikasi dalam menyimpan dan mengambil data dengan benar dari basis data menggunakan model "Item" yang 
        telah saya definisikan. Semua pengujian ini telah berhasil dilakukan, menunjukkan bahwa kode yang saya tulis berjalan sesuai 
        harapan.

        Langkah terakhir dalam proyek ini adalah memastikan repositori GitHub saya terbarui. Saya telah membuat berkas "README.md" dan 
        melakukan proses "add," "commit," dan "push" ke GitHub. Selanjutnya, saya melakukan proses deployment project "resa_lightreborn" 
        ke platform Adaptable. Saya memilih template "Python App" dengan menggunakan "PostgreSQL" sebagai basis data, serta Python 3.11 
        sebagai lingkungan pelaksanaan. Perintah "python manage.py migrate && gunicorn resa_lightreborn.wsgi" digunakan sebagai perintah 
        awal untuk menjalankan aplikasi. Situs web dapat diakses melalui domain "resalightreborn" dengan menggunakan HTTP Listener yang 
        telah diatur pada PORT. Dengan demikian, proyek saya telah berhasil di-deploy dan siap digunakan secara online.

2. Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.

    ![Bagan Resa](bagan_resa.png)

3. Jelaskan mengapa kita menggunakan virtual environment? Apakah kita tetap dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment?

    Kita menggunakan virtual environment dalam pengembangan aplikasi web berbasis Django karena itu memungkinkan kita untuk menciptakan lingkungan terisolasi yang mengelola dependensi proyek secara efisien. Ini sangat penting karena setiap proyek mungkin memerlukan versi paket Python dan dependensi yang berbeda, sehingga virtual environment membantu menghindari konflik dan masalah kompatibilitas. Tanpa virtual environment, kita dapat membuat aplikasi Django, tetapi akan terbatas dalam pengelolaan dependensi, rentan terhadap konflik, dan lebih sulit untuk menjaga kebersihan sistem. Oleh karena itu, meskipun memungkinkan, sebaiknya kita selalu menggunakan virtual environment dalam pengembangan aplikasi web Django untuk menjaga isolasi dan manajemen dependensi yang efektif.

4. Jelaskan apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya.

    MVC (Model-View-Controller), MVT (Model-View-Template), dan MVVM (Model-View-ViewModel) adalah pola desain yang digunakan dalam pengembangan perangkat lunak.

    1. MVC: Terdiri dari Model (data dan logika bisnis), View (tampilan yang diberikan kepada pengguna), dan Controller (pengendali alur aplikasi). Controller menghubungkan Model dan View.

    2. MVT: Ini adalah varian dari MVC yang digunakan dalam Django. Model sama, View mengatur logika tampilan, dan Template mengatur tampilan. "Controller" diatur oleh Django secara internal.

    3. MVVM: Digunakan dalam pengembangan aplikasi antarmuka pengguna (UI). Model adalah data dan logika, View menampilkan tampilan, dan ViewModel berperan sebagai perantara. ViewModel mengubah data dari Model agar sesuai dengan tampilan.

    Perbedaannya adalah bagaimana komponen-komponen ini berinteraksi. MVC menggunakan Controller, MVT memiliki tugas Controller internal di Django, sementara MVVM menggunakan ViewModel sebagai perantara. MVC adalah pola desain umum, MVT adalah variasi untuk Django, dan MVVM cocok untuk pengembangan aplikasi UI modern.