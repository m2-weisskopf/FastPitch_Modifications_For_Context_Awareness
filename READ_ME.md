# FastPitch Modifications For Context Awareness

Modified versions of the data_function.py, module.py and inference.py Python files from NVidia FastPitch text-to-speech
system that allows contextualised utterance embeddings to be read in as addition inputs. To use, replace data_function.py, 
module.py and inference.py in NVidia FastPitch (https://github.com/NVIDIA/DeepLearningExamples/tree/master/PyTorch/SpeechSynthesis/FastPitch) 
with their equivilants in this repository. 

The utterance embeddings are 1024 dimensional, and can be extracted from a corpus using the code in this repository: https://github.com/m2-weisskopf/generate_contextualised_utterance_embeddings_with_BART

To do inference, set the abs_path variable in the inferene.py script on line 225 to the absolute path to the directory where you store your utterance embeddings.

Filelist columns must be formatted thusly: 
audio.wav|pitch.pt|utterance_embeddding.pt|utterance_text
