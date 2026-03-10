The zip contains 5 notebooks:
-	Data&Results.ipynb
-	gemma.ipynb
-	qwen.ipynb
-	FineTuningGemma.ipynb
-	Testing_FineTuning.ipynb

First and foremost Data&Results.ipynb is the notebook that contains the part concerning data download, data exploration, visualization, preprocessing with the creation of the audio data.
The output of these elaborations is gonna be the directory ‘data’.

The gemma.ipynb and qwen.ipynb notebooks are used to do inference with the pre-trained models. The results will be saved in the directories ‘gemma’ and ‘qwen’. These directories will contain the inference results using 3 different decoding techniques: greedy, beam and temperature.

FineTuningGemma.ipynb is the notebook used to fine-tune Gemma model with text input, audio input with the test split of Xsum and SamSum datasets. Moreover it contains also the fine-tuning with different sampling rates.

Testing_FineTuning.ipynb is used to do inference with the different fine-tuned version of gemma with all the decoding techniques mentioned before.

Data&Results.ipynb then, is also used to aggregate all the results of these different inferences. So it has a part where all the predictions are cleaned and evaluated quantitatively with Rouge score and qualitatively.

This project requires a Hugging Face access token to download the model weights for qwen and gemma, the token can be saved on the Colab Secrets section to run the notebooks. For the model “unsloth/gemma-3n-E2B-it”, the token it should be added manually on the argument “token” when the model is instantiated.
<img width="499" height="451" alt="image" src="https://github.com/user-attachments/assets/5b80d5ee-8b02-401d-a804-5d71f8e44f4a" />
