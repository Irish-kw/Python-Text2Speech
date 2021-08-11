from pygame import mixer
from gtts import gTTS
import os

def bot_speak(text, lang = 'zh-tw'):
    mixer.init()
    try:
        tts = gTTS(text = text, lang = lang)
        tts.save('speak.mp3')
        mixer.music.load('speak.mp3')
        mixer.music.play()
        while(mixer.music.get_busy()):
            continue
    except:
        print('播放音效失敗')
    mixer.quit()
    os.remove('speak.mp3')

bot_speak('這是測試')
