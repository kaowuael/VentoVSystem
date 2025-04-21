# 📦 Bazowy obraz: Ubuntu 22.04
FROM ubuntu:22.04

# 🔧 Ustawienie zmiennych środowiskowych (żeby uniknąć błędów)
ENV DEBIAN_FRONTEND=noninteractive

# 🛠 Instalujemy Node.js + npm
RUN apt update && \
    apt install -y curl && \
    curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt install -y nodejs

# 📂 Katalog roboczy
WORKDIR /app

# 📄 Kopiujemy package.json i lock
COPY package*.json ./

# 📦 Instalujemy zależności (w tym dev, np. nodemon)
RUN npm install --include=dev

# 📁 Kopiujemy resztę backendu
COPY . .

# 🚀 Domyślna komenda
CMD ["node", "src/index.js"]
