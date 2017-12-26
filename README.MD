TUTORIAL MEMBUAT DOCKER COMPOUSE

1. Pertama-tama kita membuka program dockernya.
2. Kemudian login docker dengan cara
$ docker login > kemudian muncul username dan password yang anda miliki/ yang sudah dibuat di hub.docker.com
3. Membuat folder yang mengisikan dockerfile dan index.html, disini saya memberikan folder yang bernama link1.
4. Kita buat file dockerfile dengan code2 :
          FROM nginx:alpine
          COPY index.html /usr/share/nginx/html/index.html
          RUN chmod -R 755 /usr/share/nginx/html/
          VOLUME /usr/share/nginx/html/
//kemudian kita save di folder tersebut.
5. Dan membuat index.html dengan code2 sebagai berikut :
          <!DOCTYPE html>
          <html>
          <head>
          <meta charset="utf-8">
          <title>TUGAS TEORI TCC</title>
          </head>
          <body>
          <br>NAMA : RIZAL ZARDERY P P</br>
          <br>NIM : 155410042</br>
          </body>
          </html>
//lalu save di folder link1 tersebut.
6. Jika sudah dilakukan di atas kemudian kita masuk ke dockernya, lalu command ls untuk melihat isi partisi/folder .
7. Disitu banyak sekali nama-nama folder, cari folder yang bernama link1. kemudian perintah commandnya cd link1/ .
8. Command ls juga, apakah di folder link1 terdapat file dockerfile dan index.html .
9. Kemudian kita build dengan cara "docker build -t link1 ." , tunggu beberapa saat untuk mendownload file-file tersebut.
10. Jika sudah command docker pull nginx:alpine
11. jika ingin melihat perubahan sebelumnya di images nya bisa menggunakan command docker images
12. untuk meng TAG link1 menggunakan "docker tag link1 rizalzardery/link1" lalu push dengan cara "docker push rizalzardery/link"
