# Multimodal Speech Emotion Recognition Using Modality-specific Self-Supervised Frameworks

Link to the published article: [here] 

## Preparation
### Dataset
To run our code, choose between obtaining the dataset from [this link](https://sail.usc.edu/iemocap/) or accessing our preprocessed data [here](https://drive.google.com/file/d/19GcLs3k-xB1R0y1JfX14Z46uPmNKJaLX/view?usp=share). For the processed data, unzip and save it in the data folder after download. If opting for the complete IEMOCAP data, unzip it and process using the file [here](https://github.com/Ruddy202/TRANSFORMER_BASED-Emotion-Recognition)(scripts/data collected.ipynb) or use `!python mocap_data_collect.py`.

The dataset includes around ten emotions, but our study focuses on four: anger, neutral, excitement, and sadness. The processed data file exclusively contains these emotions. If you want more detected emotions, process the data independently.</p>

### How to run file:
After data processing:

1. Run any of these files (Speech, TextBERT, MotionCap)
	* Speech_Wav2vec: for training on speech only. Find fine-tuning details [here](https://www.tensorflow.org/hub/tutorials/wav2vec2_saved_model_finetuning).
    > Speech data was processed separately. 
	* TextBERT: for training on text.
	* MotionCap: for training on motion capture (Mocap_Rotate_Adam or SGD).
	* Concatenation: used to train all three modalities (speech + text + motion capture).

2. Additional files can be run for comparison purposes (Pairwise_Concat and Ablation):
 	* Pairwise_Concatenation: combines two modalities instead of three.
 	* Ablation: includes concatenation files trained using different optimizers.

### Where to run the code: 
The code can be executed on Google Colab, Kaggle, or create your own environment on your machine. 

## Reference

Please refer to our article for more details.

<pre> <p align="justify"> @INPROCEEDINGS{9520692,  
	author={Patamia, Rutherford Agbeshi and 
	Jin, Wu and Acheampong, Kingsley Nketia and 
	Sarpong, Kwabena and Tenagyei, Edwin Kwadwo},  
	booktitle={2021 IEEE 2nd International Conference on Pattern Recognition and Machine Learning (PRML)},   
	title={Transformer Based Multimodal Speech Emotion Recognition with Improved Neural Networks},   
	year={2021},  
	volume={},  
	number={},  
	pages={195-203},  
	doi={10.1109/PRML52754.2021.9520692}} </p> </pre>







