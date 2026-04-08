# ML Labs - Dmitriy Shutov

## Лабораторная работа 1: Computer Vision (Object Detection)

### Датасет
Скачать датасет: [Google Drive](https://drive.google.com/file/d/1OL5XPUmw33gfQK9BD9k6G3M9RSLRsZce/view?usp=sharing)

### Запуск в Google Colab

1. Скачать ноутбук `cv.ipynb` из папки `lab1/`
2. Загрузить его в Google Colab (File → Upload notebook)
3. Скачать датасет по ссылке выше
4. В первой ячейке ноутбука будет код для загрузки файла:
```python
from google.colab import files
files.upload()
```
5. Запустить все остальные ячейки

# Лабораторная работа 2: NLP (оценка 3)

## Установка и запуск (Windows 11)

1. Установить WSL:
wsl --install

2. Запустить Ubuntu:
wsl.exe -d Ubuntu

3. Установить Ollama:
curl -fsSL https://ollama.com/install.sh | sh

4. Запустить Ollama сервер:
ollama serve &

5. Скачать модель (в новом терминале WSL):
ollama pull qwen2.5:0.5b

6. Создать файл скрипта в WSL:
nano inference.py
(вставить код скрипта и сохранить)

7. Проверить работу Ollama:
curl -X POST http://localhost:11434/api/generate -d '{"model": "qwen2.5:0.5b", "prompt": "Hello", "stream": false}' -H "Content-Type: application/json"

8. Запустить скрипт:
python3 inference.py
