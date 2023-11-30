# Multimodal Speech Emotion Recognition Using Modality-specific Self-Supervised Frameworks

Link to the published article: [here] 



## Basic Idea:

<p align="justify"> With the procession of technology, the human-machine interaction research field is in growing need of robust automatic emotion recognition systems. Building machines that interact with humans by comprehending emotions paves the way for developing systems equipped with human-like intelligence. Previous architecture in this field often considers RNN models. However, these models are unable to learn in-depth contextual features intuitively. This paper proposes a transformer-based model that utilizes speech data instituted by previous works, alongside text and mocap data, to optimize our emotional recognition system’s performance. Our experimental result shows that the proposed model outperforms the previous state-of-the-art. The IEMOCAP dataset supported the entire experiment. </p>

-----

## Preparation
### Dataset
To run our code, you have two options: either acquire the dataset from [this link](https://sail.usc.edu/iemocap/) or access our preprocessed data [here](https://drive.google.com/file/d/19GcLs3k-xB1R0y1JfX14Z46uPmNKJaLX/view?usp=share). If you opt for the processed data, unzip the file and save it in the data folder after downloading. Alternatively, if you choose to obtain the complete IEMOCAP data from the provided link, unzip it and process it using the file found [here](https://github.com/Ruddy202/TRANSFORMER_BASED-Emotion-Recognition)(scripts/data collected.ipynb) or use `!python mocap_data_collect.py`.

The dataset encompasses approximately ten emotions. In alignment with prior research, our study specifically concentrates on four emotions: anger, neutral, excitement, and sadness. Consequently, the processed data file exclusively includes these four emotions. Should you wish to expand the range of detected emotions in your project, you'll need to process the data independently.</p>

### How to run file:
After Data is processed (NEXT):

1. Run any of these files (Speech, TextBERT, MotionCap)
	* Speech_Wav2vec: for training on speech only. For more information on how to we fine-tune wav2vec [here](https://www.tensorflow.org/hub/tutorials/wav2vec2_saved_model_finetuning).
    >speech data was processed separately. 
	* TextBERT: for training on text.
	* MotionCap: for training on motion capture(Mocap_Rotate_Adam or SGD)
	* Concatenation: for training all three modalities (speech + text + motion cap)

2. Extra files can also be executed for comparison purposes (Pairwise_Concat and Ablation)
	* Pairwise_Concatenation: combines two modalities instead of 3.


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
