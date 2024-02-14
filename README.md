<details>
<summary>MODULE 1</summary>

## Refleksi 1
Setelah meninjau kembali kode saya setelah menambahkan fitur baru menggunakan Spring Boot, saya telah memeriksa penerapan prinsip-prinsip clean code dan secure coding practices. Prinsip-prinsip ini termasuk penggunaan meaningful names untuk variabel dan fungsi, memastikan setiap fungsi hanya melakukan satu tugas, mengurangi penggunaan comment dengan menulis kode yang jelas, dan menggunakan struktur objek yang sesuai. Selain itu, saya juga telah membuat unit test dan functional test yang relevan.

Mungkin salah satu kesalahan pada kode saya adalah error handling serta authentication dan authorization yang belum diimplementasikan. Untuk memperbaiki hal ini, perlu ditambahkan penerapan error handling yang baik dan fitur keamanan tambahan seperti otentikasi dan otorisasi.

## Refleksi 2
Setelah menyusun unit test, saya merasa lebih yakin terhadap kebenaran kode saya. Jumlah unit test yang diperlukan dalam sebuah kelas tergantung pada kompleksitas fungsionalitas yang dimiliki oleh kelas tersebut. Penting untuk memastikan bahwa setiap fungsi yang ada telah diuji secara memadai untuk memverifikasi kinerja program secara keseluruhan. Code coverage adalah sebuah metrik yang bermanfaat untuk mengevaluasi sejauh mana kode telah diuji, namun mencapai 100% code coverage tidak menjamin bahwa tidak akan ada bug dalam kode. Ada kemungkinan bahwa beberapa kasus uji belum di-cover, atau mungkin ada bug yang terjadi karena logika yang salah atau asumsi yang salah dalam kode tersebut.

Untuk membuat rangkaian functional test baru yang mirip dengan yang sudah ada, mungkin perlu dipertimbangkan potensi pengulangan atau duplikasi kode. Menggabungkan prosedur pengaturan umum menjadi metode yang dapat digunakan kembali atau kelas utilitas dapat meningkatkan kebersihan dan kualitas kode secara keseluruhan. Ini akan membantu mengurangi duplikasi kode dan meningkatkan keterbacaan dan pemeliharaan kode.
</details>

<details>
<summary>MODULE 2</summary>

## Refleksi 1
Salah satu masalah yaitu terkait visibilitas yang saya atasi dengan mengubah class dan metode pengujian JUnit5 menjadi visibilitas default daripada menggunakan modifier public. Langkah ini membantu dalam menjaga isolasi pengujiannya serta mencegah akses yang tidak diinginkan. Kedua, terkait dengan injeksi field, khususnya penggunaan @Autowired atau @Inject dalam framework Spring. Hal ini tidak disarankan karena berpotensi menciptakan objek dalam keadaan tidak valid dan mempersulit pengujian. Strategi yang digunakan untuk mengatasi ini yaitu dengan mengubah objek yang menggunakan injeksi @Autowired pada file ProductServiceImpl.java dengan membuat inisiasi class secara langsung. Terakhir, saya membersihkan import yang tidak diperlukan karena dapat meningkatkan kompleksitas kode dan memperlambat proses kompilasi. Saya juga menambahkan import secara manual yang diperlukan untuk mengurangi potensi kesalahan.

## Refleksi 2
Menurut saya, implementasi saat ini telah memenuhi definisi Continuous Integration dan Continuous Deployment (CI/CD). Dengan github workflows, proyek dapat mengotomatisasi Continuous Integration (CI) dengan menjalankan test dan melakukan scan kode menggunakan SonarCloud setiap kali melakukan push ke repositori github. Selain itu,  otomatisasi Continuous Deployment (CD) akan melakukan deployment ke platform Koyeb setiap kali ada push atau pull request ke suatu branch.

</details>