# TTS-API

Text to speech REST API for multiple TTS engines.

## Setup

First, you should install the supported TTS engines:

### GoogleSpeech

```
apt install python3 sox libsox-fmt-mp3
pip install google_speech

# Run only when you need to upgrade
pip install --upgrade pip
pip install google_speech --upgrade
```

### Festival

```
apt install festival
```

### eSpeak

```
apt install espeak
```

You also need to install **nodejs** and **npm**, and then, simply run `npm install` and `npm start`.
The API should now be running at `http://localhost:3000`.

## Usage

When running, the API will receive POST request at `http://localhost:3000`.
You can use your favourite REST client to send a request, or use the built-in form.

### Built-in form

Go to `http://localhost:3000` with your browser, fill the form with data and submit it. Just that.

### Send POST request

You can send a POST request to `http://localhost:3000` following this scheme:

* **Headers**
	* **Content-Type**: `application/json`
* **Body**
	* `{ "voice": "google_speech", "textToSpeech": "hello world", "language": "en", "speed": "1" }`

## Available TTS engines

### GoogleSpeech

Google Speech is a simple multiplatform command line tool to read text using Google Translate TTS (Text To Speech) API.

You need to be online to communicate with Google servers.

Learn more at https://github.com/desbma/GoogleSpeech

### Festival

Festival is a free software multi-lingual speech synthesis workbench that runs on multiple-platforms offering black box text to speech, as well as an open architecture for research in speech synthesis.

It works offline.

Learn more at http://www.cstr.ed.ac.uk/projects/festival/ and http://festvox.org/festival/

### eSpeak

eSpeak is a compact open source software speech synthesizer for English and other languages, for Linux and Windows.

It works offline.

Learn more at http://espeak.sourceforge.net/
