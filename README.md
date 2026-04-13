# 🎙️ Transcrição de Áudio com Whisper + ChatGPT

Projeto desenvolvido no Google Colab que grava áudio, transcreve usando Whisper e responde com IA.

---

## 🚀 Funcionalidades

* 🎤 Grava áudio pelo navegador
* 🧠 Transcreve com Whisper (OpenAI)
* 💬 Gera resposta com ChatGPT
* 🔊 Converte resposta em áudio (gTTS)

---

## 🛠️ Tecnologias

* Python
* OpenAI API
* Google Colab
* gTTS

---

## ▶️ Como executar

1. Abra o notebook no Google Colab
2. Configure sua API KEY nos Secrets:

   * Nome: `OPENAI_API_KEY`
3. Execute as células na ordem

---

## 🎤 Exemplo de uso

```python
gravar_audio()
```

---

## 🧠 Transcrição com Whisper

```python
transcricao = client.audio.transcriptions.create(
    model="whisper-1",
    file=audio_file
)
```

---

## 💬 Resposta da IA

```python
resposta = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[
        {"role": "user", "content": texto_usuario}
    ]
)
```

---

## 🔊 Saída em áudio

```python
tts = gTTS(texto_resposta, lang='pt')
tts.save("resposta.mp3")
```

---

## ⚠️ Segurança

* ❌ Nunca suba sua API KEY
* 🔐 Use Secrets no Colab

---

## 📁 Estrutura

```
📦 projeto
 ├── transcricao_audio.ipynb
 └── README.md
```

---

## 👨‍💻 Autor

Leonardo 🚀
