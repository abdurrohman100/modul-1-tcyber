# modul-1-tcyber 
##Pengenalan Capture The Flags

Capture the Flag(CTF) adalah salah satu perlombaan dibidang teknologi terutama dibidang sekuritas siber. Pada perlombaan CTF kalian akan diberikan sebuah tantangan untuk mencari sebuah string yang sudah disembunyikan sistem dimana disbut dengan istilah Flag. Kompetisi CTF biasanya diikuti oleh tim beranggotakan 3 orang, tapi ada juga yang bersifat individu atau memperbolehkan anggota lebih dari 3. 

Secara umum kompetisi CTF memilikki 3 format utama yaitu Jeopardy, Attack-Defence, dan mixed. 

- Pada format Jeopardy kita diminta menyelesaikan berbagai challenges dan mendapat poin untuk setiap challenges yang berhasil kita kerjakan. Semakin susah challenges yang berhasil kita kerjakan semakin besar pula poin yang kit dapat. Pemenang dalam format Jeopardy ini adalah tim yang memiliki poin terbanyak. Challenges pada kompetisi Jeopardy sendiri memiliki banyak kategori yang akan dibahas lebih detail nanti. Kompetisi format Jeopardy ini merupakan kompetisi yang paling umum dan paling sering diadakan karena kompleksitasnya yang tidak terlalu rumit.
- Pada format Attack-Defense kita disediakan server yang memiliki vuln dan hidden flag. Kemudian setiap tim diberikan waktu untuk mengetahui celah dari server tersebut dan melakukan *patching* terhadap vuln tersbut. Objektif dari format ini adalah menjaga server kita dari serangan tim lawan dan sekaligus menyerang server tim lawan. Secara umum pemain mendapat poin ketika berhasil menghadang serangan lawan dan berhasil menyerang server tim lain. Kompetisi ini kebanyakan diadakan secara offline karena kompleksitas nya yang tinggi dan configurasi server yang cukup rumit.

- Pada kategori mixed adalah gabungan dari Jeopardy dan Attack-Defence.



##Kategori Challenges pada format Jeopardy
####Cryptography
Cryotography atau biasa disebut crypto adalah sebuah kategori challenges dimana kita diberikan soal berupa pesan pesan yang telah dienkripsi. Untuk membaca pesan tersebut kita diharuskan mencari decrytor dari enkripsi tersebut. Setelah dilakukan dekripsi biasanya kita akan mendapatkan flag yang kita cari. Beberapa jenis enkripsi yang ada antara lain Caesar Chipper, Vigenère Chipper, MD5Hash, RSA dan masih banyak lagi.


####Web
Kategori web ini memiliki banyak tujuan juga dari yang paling mudah dengan inspect element hingga problem sulit seperti meminta kita untuk mendapatkan hak akses tertentu dari sebuah web misalnya dari user biasa menjadi admin. Mengerjakan kategori ini membutuhkan pemahaman teknologi web, seperti untuk bagian interace diperlukan pemahaman html dan javascript, backend pengetahuan minimal php, database seperti dasar sql, cookie,session, HTTP,dsb. 

####Reverse Engineering
Pada kategori Reverse Engineering(RE) kita diharuskan mereverse engineer sebuah file binnary atau source code. Tujuanya untuk mendapatkan flag dari kode tersebut. Untuk mengerjakan kategori ini kita memerlukan pemahaman akan bahasa assembly dan bahasa c(memory allocation, pointer, function pointer). Tool yang biasa digunakan adalah IDA Pro atau Hopper.

####Binary Exploitation 
Binary Exploitation(BinEx) merupakan sebuah kategori dimana kita mencari celah pada sebuah program (binary) dan mengubah programnya agar tidak berjalan sesuai seharusnya. Untuk melakukan binex kita harus terlabih dahulu memehami RE untuk menemukan celah pada sebuah program binary


####Forensic
Pada kategori Forensic kita diminta untuk mengesktrak data dari sebuah file. File tersebut bisa bermacam-macam seperti  text, archived file, network capture, image, audio, memory dump, dsb. Forensic ini adalah kategori yang sangat luas dan membutuhkan pengetahuan mengenai berbagai filesystem yang ada. Beberapa tools yang digunakan pada kategori forensic adalah wireshark,binwalk,exiftool, stgesolve, volatility, audacity,dsb.


####pwnables 
Pada kategori ini kita diminta mengeksploit service yang berjalan pada remote server. pwnables ini mirip dengan reverse engineering cuma perbedaanya jika pada RE kita diberikan binary filenya, tapi pada pwnables binary file hanya berjalan pada remote server dan flag yang harus kita ambil ada dalam remote server tersebut.

####MISC
Kategori ini adalah kategori selain diatas atau gabungan dari kategori-kategori diatas.

##Mulai belajar CTF
Perlombaan CTF memiliki banyak bidang pengetahuan dan pengetahuan itu saling berkaitan. Oleh karena itu dari berbagai kategori diatas akan lebih baik jika pelajari semuanya. 
- Memiliki pengetahuan dasar tentang CTF
  - Untuk belajar CTF sangat disarankan familiar dengan sistem operasi linux, karena pada sistem operasi linux ini banyak terdapat tool-tool open source yang bisa memudahkan dalam memecahkan challenges dalam CTF.
  CLI linux :https://github.com/AZakyH/Modul-Pelatihan-Linux-2018/blob/master/CLI/README.md
  - Untuk belajar Cryptography disarankan untuk belajar scripting menggunakan python dan disarankan mencari tahu berbagai algortima enkripsi yang ada.
  - Untuk belajar Web disarankan mulai belajar dari bahasa HTML, PHP dan Javascript dan memhami cara kerja HTTP
  - Untuk belajar RE dan BinEx disarankan untuk mempelajari bahasa C dan bahasa Assembly, cobalah membuat program c kemudian coba lakukan reverse engineering terhadap program mu.
  - Untuk belajar Forensic disarankan belajar tentang filesystem
  - Untuk belajar pwnable disarankan belajar RE, BiNex dan Networking terlebih dahulu.
- Meningkatkan Skill Googling, terdapat beberapa challenges CTF yang bisa diselesaikan hanya dengan Googling
- Dan yang pasti untuk belajar CTF sangat disarankan untuk mengikuti kompetisi CTF.
  





###Referensi
http://ctfs.github.io/resources/
https://blog.compactbyte.com/2014/04/24/security-ctf/




