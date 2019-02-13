                   (_)     | |                  
          _ __ __ _ _ _ __ | |__   _____      __
(./\_/\  | '__/ _` | | '_ \| '_ \ / _ \ \ /\ / /
.)>^,^<  | | | (_| | | | | | |_) | (_) \ V  V / 
(__(__)  |_|  \__,_|_|_| |_|_.__/ \___/ \_/\_/ 

# rainbow
Project rainbow, aka kill-Alexa 

My idea is to get an end-to-end local version of not-Alexa running without a gpu (as long as possible). So far, the solution includes:

* speech-to-text courtesy of [Mozilla's DeepSpeech](https://github.com/mozilla/DeepSpeech)
* text similarity using of [gensim](https://pypi.org/project/gensim/)
* text-to-speech using old-school tech in `pico2wave` (neural networks, pre-trained, just take too long to do the conversion without a gpu)

The functionality with be logic with fuzziness using word similarity. For starters, the main commands I need to kill Alexa are:

* set timer for N [and a half] minutes
* what's the forecast for today?

DeepSpeech often misinterprets `timer` as `time or`, but otherwise understands me well.
