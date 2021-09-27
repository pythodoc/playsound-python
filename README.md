# install pyttsx3 on pip using command "pip install pyttsx3" it can only install linux this code
# can't run in windows for windows install & use "Sapi5" install using commmand "pip install sapi5"
import pyttsx3

engine = pyttsx3.init()
text = "Github Rocks"
engine.say(text)
# play the speech
engine.runAndWait()

# can set the rate of speed for the speech Syntesis
rate = engine.getProperty("rate")
print(rate)

engine.setProperty("rate", 100)
engine.say(text)
engine.runAndWait()

# choose the voices in linux Repository in id 
#voices = engine.getProperty("voices")
#print(voices)
# it can also be set as voice id wheather you need desired voice to talk
#engine.setProperty("voice", voices[1].id)
#engine.say(text)
#engine.runAndWait()

# saving the file in the form of any audio format .mp3,.wav,.AC3,etc
engine.save_to_file(text, "python.mp3")
engine.runAndWait()
