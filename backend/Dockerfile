# 📦 Bazowy obraz z Node.js LTS
FROM node:18

# 📂 Katalog roboczy w kontenerze
WORKDIR /app

# 📄 Kopiujemy package.json i package-lock.json (jeśli jest)
COPY package*.json ./

# 🧱 Instalujemy zależności
RUN npm install

# 📁 Kopiujemy resztę plików backendu do kontenera
COPY . .

# 🚀 Domyślna komenda do uruchomienia backendu
CMD ["npm", "run", "dev"]