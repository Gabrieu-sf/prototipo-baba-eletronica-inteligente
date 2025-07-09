# 👶📹 Babá Eletrônica com Inteligência Artificial

Este projeto é um sistema de **monitoramento infantil com IA**, desenvolvido em Python, que utiliza **visão computacional com YOLO** para detectar se uma criança está dentro ou fora do berço, emitindo alertas em caso de perigo.

---

## 🧠 Tecnologias Utilizadas

- **Python 3**
- **YOLO** (modelo personalizado `.pt`)
- **OpenCV** – Processamento de vídeo
- **Tkinter** – Janela de alerta visual
- **Pygame** – Emissão de som
- **Threading** – Execução paralela de alertas
- **NumPy** – Manipulação de coordenadas da área segura

---

## 🎯 Objetivo

Detectar em tempo real, a partir de um vídeo ou webcam, se uma criança ultrapassa os limites definidos do berço. Caso isso ocorra por mais de 5 segundos, o sistema emite:

- Um **som de alerta**;
- Uma **janela popup** com aviso visual;
- E encerra o programa automaticamente (pode ser modificado para continuar).

---

## 🔧 Como Funciona

1. A câmera (ou vídeo) é processada quadro a quadro;
2. O modelo YOLO detecta a presença da criança (classe `person`);
3. Uma região é definida como o "berço" usando coordenadas poligonais;
4. Se a criança estiver fora dessa área por mais de 5 segundos:
   - É exibido um alerta visual (Tkinter),
   - Um som é reproduzido (Pygame),
   - E o programa é finalizado.

---

## 🗂️ Estrutura

project/
│
├── modelo/
│ └── yolo11s.pt
├── videos/
│ └── video.mp4
├── audio/
│ └── sound_alert.mp3
├── main.py
└── README.md


---

## ▶️ Como Usar

1- Clone o repositório:
   git clone https://github.com/seuusuario/baba-eletronica-ia.git
   
2- Instale as dependências:
pip install ultralytics opencv-python pygame numpy

3- Coloque seu vídeo em videos/video.mp4 e seu modelo .pt em modelo/.

4- Execute o script:
python main.py
