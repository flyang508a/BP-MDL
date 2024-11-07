# BP-MDL

This code consists N parts:

1. ppg_analy.py: The PPG signal preprocessing and analysis code. [Hsieh, T.-H.]
2. Signal_pairing.ipynb: PPG waveform segmentation、feature extraction、pairing mechanism and [Mekonne, B., Lu, W.-R.]
3. MDL_SYS.ipynb / MDL_DIA.ipynb: The Mixed Deduction Learning code for Systolic/Diatolic prediction [Mekonne, B., Lu, W.-R.]
4. MIL_SYS.ipynb / MIL_DIA.ipynb: The Mixed Induction Learning code for Systolic/Diatolic prediction [Mekonne, B., Lu, W.-R.]
5. PIL_SYS.ipynb / PIL_DIA.ipynb : The Personalized Deduction Learning code for Systolic/Diastolic prediction [Mekonne, B., Lu, W.-R.]
6. PDL.ipynb : The Personalized Deduction Learning code for both Systolic and Diastolic prediction [Mekonne, B., Lu, W.-R.]

Name in [ ] indicates the primary contributors.

Article Authors: Bitewulign Kassa Mekonnen, Wei‑Ru Lu, Tung‑Han Hsieh, Justin Chu ,and Fu‑Liang Yang
Research Center for Applied Sciences, Academia Sinica. 

Article: https://doi.org/10.1038/s41598-024-75583-y

## ppg_analy.py:

To use this code, the system should install python (>= 3.5), python modules numpy, scipy, and gnuplot.

This code reads the index file "sub_info*.txt", from which find the PPG signal data files, and proceed the signal analysis. The PPG signals consist Left hand, Right hand, each measured with IR and RD. The code parameters are configurable through the config file "ppg_input.txt". The code outputs the following data files:
* *_signal.txt: The denoised AC and DC singals of the raw PPG signal.
* *_minmax.txt: The indices of pulse separation of the PPG AC signal.
* *_peak.txt, *_peaklist.txt, *_dA1res.txt: The morphological features of pulse waveform extracted from the PPG AC signal.
* *_sigIRFT.txt, *_sigRDFT.txt: The Fourier transformed data of the PPG AC signal.
* *_step.txt: The summarized list of extracted morphological features.
To run this code, please put "ppg_analy.py" and "ppg_input.txt" in the same working directory, and run the command:

        python3 ./ppg_analy.py <full path of sub_info file>
  
## Signal_pairing.ipynb:
Based on the output files of ppg_analy.py, this file includes functions for pulse wave segmentaiton, featureing, and output the file with paired PPG pulse.

## MDL_SYS/DIA.ipynb:
File includes the MDL model and training/testing fork flow.



## MIL_SYS/DIA.ipynb:
File includes the MIL model and training/testing fork flow.

## PIL_SYS/DIA.ipynb:
File includes the MDL model and training/testing fork flow.

## PDL.ipynb:
File includes the MDL model and training/testing fork flow.

Currently, we have parts 1-3 ready for posting on github, and the other parts are still under checking and preparation. Remainig files will be posted as soon as they are ready.
