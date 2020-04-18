# modul-1-tcyber 
## Pengenalan Capture The Flags

Capture the Flag(CTF) adalah salah satu perlombaan dibidang teknologi terutama dibidang sekuritas siber. Pada perlombaan CTF kalian akan diberikan sebuah tantangan untuk mencari sebuah string yang sudah disembunyikan sistem dimana disbut dengan istilah Flag. Kompetisi CTF biasanya diikuti oleh tim beranggotakan 3 orang, tapi ada juga yang bersifat individu atau memperbolehkan anggota lebih dari 3. 

Secara umum kompetisi CTF memilikki 3 format utama yaitu Jeopardy, Attack-Defence, dan mixed. 

- Pada format Jeopardy kita diminta menyelesaikan berbagai challenges dan mendapat poin untuk setiap challenges yang berhasil kita kerjakan. Semakin susah challenges yang berhasil kita kerjakan semakin besar pula poin yang kit dapat. Pemenang dalam format Jeopardy ini adalah tim yang memiliki poin terbanyak. Challenges pada kompetisi Jeopardy sendiri memiliki banyak kategori yang akan dibahas lebih detail nanti. Kompetisi format Jeopardy ini merupakan kompetisi yang paling umum dan paling sering diadakan karena kompleksitasnya yang tidak terlalu rumit.
- Pada format Attack-Defense kita disediakan server yang memiliki vuln dan hidden flag. Kemudian setiap tim diberikan waktu untuk mengetahui celah dari server tersebut dan melakukan patching terhadap vuln tersbut. Objektif dari format ini adalah menjaga server kita dari serangan tim lawan dan sekaligus menyerang server tim lawan. Secara umum pemain mendapat poin ketika berhasil menghadang serangan lawan dan berhasil menyerang server tim lain. Kompetisi ini kebanyakan diadakan secara offline karena kompleksitas nya yang tinggi dan configurasi server yang cukup rumit.
- Pada kategori mixed adalah gabungan dari Jeopardy dan Attack-Defence.

Biasanya pada perlombaan CTF kita akan diminta untuk menuliskan langkah-langkah kita dalam mengerjakan challenges yang berhasil kita solve, hal ini kemudian akan disebut Write Up.

## Kategori Challenges pada format Jeopardy
### Cryptography
Cryotography atau biasa disebut crypto adalah sebuah kategori challenges dimana kita diberikan soal berupa pesan pesan yang telah dienkripsi. Untuk membaca pesan tersebut kita diharuskan mencari decrytor dari enkripsi tersebut. Setelah dilakukan dekripsi biasanya kita akan mendapatkan flag yang kita cari. Beberapa jenis enkripsi yang ada antara lain Caesar Chipper, Vigenère Chipper, MD5Hash, RSA dan masih banyak lagi.

>Contoh Challenges dari picoCTF
>##### The numbers
>Point: 50
>##### Category
>Cryptography
>##### Question
>The [numbers](https://2019shell1.picoctf.com/static/eb3589c566dd3f809908053460acb817/the_numbers.png) [(link)](https://2019shell1.picoctf.com/static/eb3589c566dd3f809908053460acb817/the_numbers.png)... what do they mean?





### Web
Kategori web ini memiliki banyak tujuan juga dari yang paling mudah dengan inspect element hingga problem sulit seperti meminta kita untuk mendapatkan hak akses tertentu dari sebuah web misalnya dari user biasa menjadi admin. Mengerjakan kategori ini membutuhkan pemahaman teknologi web, seperti untuk bagian interace diperlukan pemahaman html dan javascript, backend pengetahuan minimal php, database seperti dasar sql, cookie,session, HTTP,dsb. 
>Contoh Challenges dari picoCTF
>##### Insp3ct0r
>Point: 50
>##### Category
>Web Exploitation
>##### Question
>Kishor Balan tipped us off that the following code may need inspection: https://2019shell1.picoctf.com/problem/52962/ [(link)](https://2019shell1.picoctf.com/problem/52962/) or http://2019shell1.picoctf.com:52962



#### Reverse Engineering
Pada kategori Reverse Engineering(RE) kita diharuskan mereverse engineer sebuah file binnary atau source code. Tujuanya untuk mendapatkan flag dari kode tersebut. Untuk mengerjakan kategori ini kita memerlukan pemahaman akan bahasa assembly dan bahasa c(memory allocation, pointer, function pointer). Tool yang biasa digunakan adalah IDA Pro atau Hopper.
>Contoh Challenges dari picoCTF
>##### vault-door-1
>Point: 100
>##### Category
>Reverse Engineering
>##### Question
>This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://2019shell1.picoctf.com/static/e34a3f6d6e6341be2f9f562f1b4e7c33/VaultDoor1.java)

#### Binary Exploitation 
Binary Exploitation(BinEx) merupakan sebuah kategori dimana kita mencari celah pada sebuah program (binary) dan mengubah programnya agar tidak berjalan sesuai seharusnya. Untuk melakukan binex kita harus terlabih dahulu memahami RE untuk menemukan celah pada sebuah program binary.
Contoh Challenges dari picoCTF
>##### handy-shellcode
>Point: 50
>##### Category
>Binary Exploitation
>#### Question
>This [program](https://2019shell1.picoctf.com/static/f5f38a3523dffd5f487719d1f35815a0/vuln) executes any shellcode that you give it. Can you spawn a shell and use that to read the flag.txt? You can find the program in /problems/handy-shellcode_1_ebc60746fee43ae25c405fc75a234ef5 on the shell server. [Source](https://2019shell1.picoctf.com/static/f5f38a3523dffd5f487719d1f35815a0/vuln.c).


#### Forensic
Pada kategori Forensic kita diminta untuk mengesktrak data dari sebuah file. File tersebut bisa bermacam-macam seperti  text, archived file, network capture, image, audio, memory dump, dsb. Forensic ini adalah kategori yang sangat luas dan membutuhkan pengetahuan mengenai berbagai filesystem yang ada. Beberapa tools yang digunakan pada kategori forensic adalah wireshark,binwalk,exiftool, stgesolve, volatility, audacity,dsb.
>Contoh Challenges dari picoCTF
>##### So Meta
>Point: 150
>##### Category
>Forensic
>##### Question
>Find the flag in this [picture](https://2019shell1.picoctf.com/static/ddffae2f670f7c822c4f878e932bf6c5/pico_img.png). You can also find the file in /problems/so-meta_0_7c0b2ae7a38b024c6b1c68cf50970a88.


#### pwnables 
Pada kategori ini kita diminta mengeksploit service yang berjalan pada remote server. pwnables ini mirip dengan reverse engineering cuma perbedaanya jika pada RE kita diberikan binary filenya, tapi pada pwnables binary file hanya berjalan pada remote server dan flag yang harus kita ambil ada dalam remote server tersebut.
Contoh Write Up Challenges [hangman](https://github.com/ChaO-0/WriteUps/tree/master/Arkavidia/2020/quals/pwn/hangman) Penyisihan Arkavidia 2020]

#### MISC
Kategori ini adalah kategori selain diatas atau gabungan dari kategori-kategori diatas.

## Mulai belajar CTF
Perlombaan CTF memiliki banyak bidang pengetahuan dan pengetahuan itu saling berkaitan. Oleh karena itu dari berbagai kategori diatas akan lebih baik jika pelajari semuanya. 
- Memiliki pengetahuan dasar tentang CTF
  - Untuk belajar CTF sangat disarankan familiar dengan sistem operasi linux, karena pada sistem operasi linux ini banyak terdapat tool-tool open source yang bisa memudahkan dalam memecahkan challenges dalam CTF.
  berikut ada beberapa [CLI dasar linux](https://github.com/AZakyH/Modul-Pelatihan-Linux-2018/blob/master/CLI/README.md).
  - Untuk belajar Cryptography disarankan untuk belajar scripting menggunakan python dan disarankan mencari tahu berbagai algortima enkripsi yang ada.
  - Untuk belajar Web disarankan mulai belajar dari bahasa HTML, PHP dan Javascript dan memhami cara kerja HTTP
  - Untuk belajar RE dan BinEx disarankan untuk mempelajari bahasa C dan bahasa Assembly, cobalah membuat program c kemudian coba lakukan reverse engineering terhadap program mu.
  - Untuk belajar Forensic disarankan belajar tentang filesystem
  - Untuk belajar pwnable disarankan belajar RE, BiNex dan Networking terlebih dahulu.
- Meningkatkan Skill Googling, terdapat beberapa challenges CTF yang bisa diselesaikan hanya dengan Googling
- Dan yang pasti untuk belajar CTF sangat disarankan untuk mengikuti kompetisi CTF.

## Resource Untuk Belajar CTF


- [CTFTime](https://ctftime.org/) menyediakan info mengenai berbagai kompetisi CTF.
- [Referensi CTF101](https://ctf101.org/) terdapat materi mengenai pengetahuan dasar CTF.
- [Referensi Trailofbits](https://trailofbits.github.io/ctf/) Terdapat tips & trick menganalisa file terutama untuk forensic
- [Referensi Tool](https://github.com/apsdehal/awesome-ctf) Referensi tools untuk CTF
- [picoCTF2019](https://github.com/apsdehal/awesome-ctf) Open Contest dimana kamu bisa mulai berlatih CTF.
- [CTFLearn](https://ctflearn.com/dashboard) salah satu open contest juga dengan variasi challenges yang banyak.

### Referensi
http://ctfs.github.io/resources/

https://blog.compactbyte.com/2014/04/24/security-ctf/

https://2019game.picoctf.com/problems

https://github.com/ChaO-0/WriteUps/tree/master/Arkavidia/2020/quals/pwn/hangman

https://fareedfauzi.github.io/ctfonline/#


