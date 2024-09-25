## NAMA : LOUISE OLIVIA PANGGABEAN
## NIM : 09011282328032
## KELAS : SK3B

# LAPORAN PRAKTIKUM SISTEM OPERASI (JOB CONTROL)
### 1. Eksekusi seluruh profile yang ada :  
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :
echo “Profile dari /etc/profile”

**HASIL :**

<img src ="https://github.com/user-attachments/assets/50c90939-adbe-40f2-b13d-55a6927f7ea7" width=500/>
<img src ="https://github.com/user-attachments/assets/6d61ea8b-5dd2-4046-879f-2e822a2bd9ea" width=500/> 


**PENGECEKKAN :**

<img src ="https://github.com/user-attachments/assets/74cf5716-df0e-43d7-97ef-536f160213e5" width=500/> 


b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :

/home/stD02001/.bash_profile

/home/. stD02001/.bash_login

/home/mahasiswa/.profile

/home/mahasiswa/.bashrc 

 **HASIL :**
 
 <img src ="https://github.com/user-attachments/assets/40e3dbd3-ca35-4edb-8aa0-cb2c6593c5fc" width=500/> 


Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :

echo “Profile dari .bash_profile”

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang
bersangkutan.

**HASIL :**
1. /home/louise/.bash_profile
<img src ="https://github.com/user-attachments/assets/ac82022a-4590-4083-83d3-33ae0b549b6b" width=500/> 


2. /home/louise/.bash_login
<img src ="https://github.com/user-attachments/assets/eca600b7-200c-4922-8c82-3cb8fc64702a" width=500/> 


3. /home/louise/.profile
<img src ="https://github.com/user-attachments/assets/2f3d0d4d-53d9-4c42-a410-c3a79ad3dc9b" width=500/>


4. /home/louise/.bashrc
<img src ="https://github.com/user-attachments/assets/7eb45a73-ca91-4d76-8bf3-7fdf4c590150" width=500/>

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

$ su mahasiswa

$ exit

kemudian gunakan opsi – sebagai berikut :

$ su – mahasiswa

$ exit

Jelaskan perbedaan kedua utilitas tersebut.

**HASIL :**

<img src ="https://github.com/user-attachments/assets/f44b1a9b-7eab-4107-ac6b-7e158e828f46" width=500/>

**PENJELASAN :**
su louise hanya mengganti pengguna menjadi louise, tetapi tidak mengubah pengaturan lingkungan kerja seperti varibel atau konfigurasi yang digunakan pada pengguna louise sedangkan su - louise mengganti pengguna menjadi louise dan juga memuat semua pengaturan serta lingkungan kerja yang biasa digunakan pengguna louise saat login.

## 2. Prompt String (PS) :

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell

PS1=‟>"

export PS1

**HASIL :**

<img src ="https://github.com/user-attachments/assets/295faaf0-9f97-4127-b869-f812a8fcfa4c" width=500/><br/>

<img src ="https://github.com/user-attachments/assets/bb61c83d-02cb-47e5-9a23-e04cbe561b90" width=500/>


b. Eksperimen hasil PS1 :

$ PS1=“\! > “

69 > PS1=”\d > “

Mon Sep 23 > PS1=”\t > “

10:10:20 > PS1=”Saya=\u > “

Saya=mahasiswa > PS1=”\w >”

~ > PS1=\h >”

**HASIL :**

<img src ="https://github.com/user-attachments/assets/e9e8ca86-f427-4451-8635-08e0b98898c4" width=500/>

### 3. Logout :
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout

Echo “Terima kasih atas sesi yang diberikan”

Sleep 5

clear

**HASIL :**

<img src ="https://github.com/user-attachments/assets/382cdaa1-a4bd-4417-b132-0fb17c667d1a" width=500/> <br/>
<img src ="https://github.com/user-attachments/assets/0194bfd5-b49d-43a6-9961-4e34ca3a8e24" width=500/> <br/>

**PENGECEKKAN :**

<img src ="https://github.com/user-attachments/assets/039ad036-8f3e-415e-8285-7d39511a4bd0" width=500/> 



## 4. Bash script :
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

**HASIL :**

<img src ="https://github.com/user-attachments/assets/c3b1d392-6883-488d-bf25-4e9d711d39c0" width=500/>

p1.sh

#! /bin/bash

echo “Program p1”

ls –l

**HASIL :**

<img src ="https://github.com/user-attachments/assets/b38e8f28-4119-443e-97ce-f5683f3fcd29" width=500/>


p2.sh

#! /bin/bash

echo “Program p2”

who

**HASIL :**

<img src ="https://github.com/user-attachments/assets/8f5d70ce-8bbb-44d2-81b1-8fb693efacb1" width=500/>


p3.sh

#! /bin/bash

echo “Program p3”

ps x

**HASIL :**

<img src ="https://github.com/user-attachments/assets/e5d4f5ff-3b3d-4ef5-be89-712d5930dd72" width=500/>


b. Jalankan script tersebut sebagai berikut :

$ ./p1.sh ; ./p3.sh ; ./p2.sh

**HASIL :**

<img src ="https://github.com/user-attachments/assets/d03196f3-27ff-4162-8c24-45de0061a12b" width=500/>

$ ./p1.sh &

**HASIL :**

<img src ="https://github.com/user-attachments/assets/7ac8610e-eaf2-4ed8-98dc-425c58e0a475" width=500/>


$ ./p1.sh $ ./p2.sh & ./p3.sh &

**HASIL :**

<img src ="https://github.com/user-attachments/assets/ff9afa68-53c6-49ed-987b-1fc02656ac76" width=500/>

$ ( ./p1.sh ; ./p3.sh ) &

**HASIL :**

<img src ="https://github.com/user-attachments/assets/44656590-6c1c-4ab2-b0e4-4f2b5a798e9c" width=500/>



## 5. Jobs :
a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh,setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.
#!/bin/bash

while [ true ]

do

date >> hasil

sleep 10

done

**HASIL :**

- NAMA FILE
<img src ="https://github.com/user-attachments/assets/34e598fe-d736-495e-a687-37536cf13cee" width=500/>

- Script File
<img src ="https://github.com/user-attachments/assets/81dd6110-2706-4757-9e9e-467d57509905" width=500/>

b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background
sebagai berikut :

$ jobs

**HASIL :**

<img src ="https://github.com/user-attachments/assets/be41ad00-8eeb-4115-bcca-d9150e161ec6" width=500/>

$ find / -print > files 2>/dev/null &

$ jobs

**HASIL :**

<img src ="https://github.com/user-attachments/assets/04ba2dec-ea02-4039-9c5b-0b27029317b0" width=500/>


c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke
background

$ fg %1

$ bg

**HASIL :**

<img src ="https://github.com/user-attachments/assets/045ee538-56c6-4050-914f-f8fd07cdf5dc" width=500/>



d. Stop program background dengan utilitas kil

- $ ps x

**HASIL :**

<img src="https://github.com/user-attachments/assets/5ce1300e-1e4a-4645-8bcb-2a05bede8d2e" width=500 />


- $ kill [Nomor PID]

**HASIL :**

<img src="https://github.com/user-attachments/assets/ade8e02f-c1aa-4eb8-8399-d41129aa8d33" width=500 />


## 6. History :

a. Ganti nilai HISTSIZE dari 1000 menjadi 20

- $ HISTSIZE=20
<img src="https://github.com/user-attachments/assets/ee965632-0da5-4436-8be9-8b05a37841ee" width=500 />

- $ h
<img src="https://github.com/user-attachments/assets/5c6e9526-4ae3-4eda-a16c-b92baa982a78" width=500 />


b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir
dilakukan

$ !-5

**HASIL :**

<img src="https://github.com/user-attachments/assets/6f9e366c-bee1-4f89-8c7a-6a7b35cec8ec" width=500 />



c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer

$ !!

**HASIL :**

<img src="https://github.com/user-attachments/assets/accecb19-6680-43a9-8f05-20d1e06bf109" width=500 />


d. Ulangi instruksi pada history bufer nomor 150

$ !150

**HASIL :**

<img src="https://github.com/user-attachments/assets/3a7f4d42-e45f-4860-a1ac-b451812a4d19" width=500 />


e. Ulangi instruksi dengan prefix “ls”

$ !ls

**HASIL :**

<img src="https://github.com/user-attachments/assets/f87caca7-835a-46bc-aa2a-39bd3dfe0093" width=500 />



