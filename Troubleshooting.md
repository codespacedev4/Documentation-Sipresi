# Troubleshooting

## Jika server mati bagaimana?

Kami sudah punya mekanisme auto start di dalam docker nya, jadi tidak perlu panik, server akan jalan otomatis ketika pc dinyalakan, namun kalian perlu melakukan beberapa hal.

- buka ngrok, biasanya ada di folder server, terdapat folder ngrok, klik 2 kali pada file, maka akan terbuka terminal.
- jalankan perintah `ngrok http {port}`, maka server akan di forward oleh ngrok, kamu akan mendapatkan url, biasanya bentuk nya seperti ini `https://strongman-gratify-uneasily.ngrok-free.dev`.
- lalu buka env frontend, biasanya ada dalam folder frontend, lalu ubah `VITE_API_URL`, isi dengan url yang didapati dari ngrok dengan `/api` di belakangnya, contoh `VITE_API_URL=https://strongman-gratify-uneasily.ngrok-free.dev/api`.
- lalu jalankan perintah `git add .` dan `git push origin main`.
- lalu kalian buka vercel web nya di chrome, masuk menu settings lalu ke environment variable, lalu set `VITE_API_URL` dengan url yang didapat dari ngrok.
