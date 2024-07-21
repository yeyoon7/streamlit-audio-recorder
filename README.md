# Streamlit Audio Recorder

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://audiorecorder.streamlit.app/)
[![Generic badge](https://img.shields.io/badge/PyPI-pip_install_streamlit--audiorec-black.svg)](https://pypi.org/project/streamlit-audiorec/)
[![Generic badge](https://img.shields.io/badge/Package-v0.1.3-blue.svg)](https://pypi.org/project/streamlit-audiorec/)
[![GitHub license](https://img.shields.io/badge/Licence-MIT-gr.svg)](https://github.com/stefanrmmr/streamlit-audio-recorder/blob/main/LICENCE)


Custom component, implemented by [Stefan Rummer](https://www.linkedin.com/in/stefanrmmr/), <br/>
based on [doppelgunner](https://github.com/doppelgunner/audio-react-recorder/) 's [Audio-React-Recorder](https://www.npmjs.com/package/audio-react-recorder/) <br/>


![Screenshot 2022-05-16 at 16 58 36](https://user-images.githubusercontent.com/82606558/168626886-de128ffa-a3fe-422f-a748-395c29fa42f9.png) <br/>

## Features & Specs
- Manage access to the user's microphone via the **browser's Media-API**
- Record, playback and revert audio-recordings in apps **deployed to the web**
- Download the final recording to your local system! - **WAV, 16 bit, 44.1 kHz**
- Directly return audio recording-data to Python backend! - **arrayBuffer format**<br>

## Setup & How to Use
**1.** PIP Install the component (download from PyPI)
```
pip install streamlit-audiorec
```
**2.** Import and Initialize the component (at the top of your script)
```python
from st_audiorec import st_audiorec
```
**3.** Add an Instance of the audio recorder to your streamlit app's code.
```python 
wav_audio_data = st_audiorec()

if wav_audio_data is not None:
    st.audio(wav_audio_data, format='audio/wav')
```
**4. Enjoy recording audio inside your streamlit app! 🎈**

Feel free to reach out to me in case you have any questions! <br>
Pls consider leaving a `star` ☆ with this repository to show your support.

## 한글 버전 스트림릿 적용법 (버튼을 한글로 바꾼 상태임!)
**1.** 작업 중인 디렉토리 하위에 'streamlit-audio-recorder' 디렉토리 복사

**2.** Frontend 의존성 설치 및 bulid
 1) 의존성 설치
    ```python
    cd 작업중인디렉토리이름/streamlit-audio-recorder/frontend
    npm install
    ```
 2) 환경 변수 설정 :  NODE_OPTIONS 환경 변수를 설정하여 OpenSSL의 레거시 암호화 기능을 활성화해야함
    ```python
    export NODE_OPTIONS=--openssl-legacy-provider
    ```
 3) 빌드
     ```python
    npm run build
    ```

**3.** 패키지 설치
 1) setup.py 파일이 있는 디렉토리로 이동
    ```python
    cd 작업중인디렉토리이름/streamlit-audio-recorder
    ```
 2) 패키지 설치
    ```python
    pip install -e .
    ```

**4.** __init__.py 파일 자체를 수정한거라서 from st_audiorec import st_audiorec 로 임포트해도 한국어 버튼 나옴
 
