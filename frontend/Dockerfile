# Menggunakan image Node.js versi terbaru sebagai base image
FROM node:20

# Menetapkan direktori kerja di dalam container
WORKDIR /usr/src/app

# Menyalin file package.json dan package-lock.json (jika ada)
COPY package*.json ./

# Menginstal dependencies terlebih dahulu agar cache digunakan jika tidak ada perubahan pada package*.json
RUN npm install

# Menyalin seluruh source code ke dalam container
COPY . .

# Mengekspos port yang digunakan oleh aplikasi
EXPOSE 5173

# Menjalankan aplikasi menggunakan Vite dev server
CMD ["npm", "run", "dev", "--host"]
