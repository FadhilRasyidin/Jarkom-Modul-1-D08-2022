## Anggota Kelompok

- Mohammad Fadhil Rasyidin Parinduri // 5025201131
- Marcelino Salim // 5025201026
- Aisyah Nurhalimah // 5025201081 (menang basket lawan ftk)

### Soal Shift
- [link](https://docs.google.com/document/d/1e5fXdleV59vFthVeK0O5WfmuOYV6xi6WkpHsZEiBofE/edit?usp=sharing)

Kendala:
1. password decrypt nguli coy
2. nemu logic buat download raw file lama
3. nemu fungsi follow TCP juga lama
4. gak yakin apakah yang dicari judul ta atau topik ta

# Laporan Resmi
### Soal Nomor 1
### Soal Nomor 2
![image](https://user-images.githubusercontent.com/73109893/191791803-4dd25f6e-195f-4a02-b0ac-d8f69c304033.png)
![image](https://user-images.githubusercontent.com/73109893/191792094-b23e5d24-6d17-4359-904d-064cb12e8581.png)
- [web topik montanya](http://monta.if.its.ac.id/index.php/topik/detailTopik/194) | Topik TA (its.ac.id) Evaluasi unjuk kerja User Space Filesystem (FUSE)
##### Cara Pengerjaan
Tujuan: Mencari judul TA yang dibuka mas ishaq
1. gunakan filter `http contains monta`
2. sesuai hint dalam soal terdapat web page yang mengandung "detail topik"
3. telusuri webpage tersebut melalui wireshark kemudian buka melalui browser
4. muncul webpage dan judul/topik ta
### Soal Nomor 3
### Soal Nomor 4
### Soal Nomor 5
### Soal Nomor 6
### Soal Nomor 7
##### Cara Pengerjaan
Tujuan: Memfilter untuk mengambil paket yang berasal dari ip laptop
1. Mengetahui ip kita sendiri

![image](https://user-images.githubusercontent.com/90826711/191940577-d6cc699f-e143-4346-be31-fcbeec079fb8.png)

2. Melakukan capture filter di wireshark dengan filter src host (isi dengan ip kita). Dalam kasus ini src host 192.168.164.57

![image](https://user-images.githubusercontent.com/90826711/191940894-24124e0b-c85d-48dd-a911-604edb5d894d.png)

3. Maka didapatkan hasil

![image](https://user-images.githubusercontent.com/90826711/191941036-6c4baa9d-c9d8-41d5-b391-6926060df492.png)

### Soal Nomor 8
![image](https://user-images.githubusercontent.com/73109893/191796528-e0d76d10-b3da-44ed-b2c8-f3c64064d0a6.png)
##### Cara Pengerjaan
Tujuan: sadap dua mahasiswa yang sus xixi
1. cari pola percakapan dari kode ascii yang ditunjukkan wireshark, telusuri pelan-pelan
2. setelah menemukan polanya kita tahu bahwa internet protocol yang digunakan adalah TCP dengan filter address yang keluar atau masuk ke ip 127.0.0.1 dan 127.0.1.1
3. kemudian follow tcp stream
4. muncul percakapan mereka yang sussy
### Soal Nomor 9
##### Cara Pengerjaan
Tujuan: temukan file sussy
1. terdapat hint dari percakapan sebelumnya (di nomor 8) bahwa terdapat salted file yang dikirim dari port 9002

![image](https://user-images.githubusercontent.com/73109893/191798365-f314091f-7d49-48fa-b069-20275455c823.png)

2. follow TCP stream tersebut kemudian download RAW file dari TCP stream tersebut (karena RAW file merupakan file dengan format aslinya makanya RAW == mentah)

![image](https://user-images.githubusercontent.com/73109893/191798997-dd4d782c-fcd5-49e2-9194-048214c687a9.png)

3. save, kemudian kita cek aj y kan tipe file ny, dan wow benar ini dia file yang di-encrypt yah (cek tipe file dgn komen linuk `file [nama file]`)

![image](https://user-images.githubusercontent.com/73109893/191799224-a161db52-5dcb-46fe-9915-a17519b18fc0.png)

4. rename jadi `D08.des3` (seperti yang diminta soal)

![image](https://user-images.githubusercontent.com/73109893/191799406-f5faf5ed-09b7-4ca0-b088-190d600f798b.png)

5. Decrypt file `.des3` dengan password *nakano* (keluarga nakano, marga si keluarga kembar lima. lagi-lagi wibu) dengan output file `flag.txt`

![image](https://user-images.githubusercontent.com/73109893/191799567-a36c6173-b8bf-40b9-b7bc-a911e55ff4b8.png)

6. File `D08.des3` decrypted

![image](https://user-images.githubusercontent.com/73109893/191799854-3dcaa802-480a-4595-be89-c0297f0334ff.png)

### Soal Nomor 10

![image](https://user-images.githubusercontent.com/73109893/191800341-6d351f3b-3189-41da-985a-980326ff13a3.png)

Tujuan: menemukan password rahasia (flag) dari organisasi bawah tanah
1. buka `flag.txt` yang di-decrypt dari `D08.des3`
2. flag berupa text
> JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}
