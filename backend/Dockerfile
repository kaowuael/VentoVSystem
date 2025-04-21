# 📦 Bazowy obraz z Node.js LTS
FROM node:18

# 📂 Katalog roboczy w kontenerze
WORKDIR /app

# 📁 Kopiujemy wszystkie pliki na raz (w tym package.json + src/)
COPY . .

# 🧱 Instalujemy zależności, w tym dev (nodemon, itp.)
RUN npm install --include=dev

# 🚀 Domyślna komenda do uruchomienia backendu
CMD ["node", "src/index.js"]
