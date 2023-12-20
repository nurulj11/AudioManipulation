# Audio manipulation 

These sets of codes were used to manipulate a list of approximately 460 audio files that were used for the development of the Singapore Malay Speech Audiometry research project by the Otolaryngology Department of the National University of Singapore. The overall goal of these codes is to adjust each file's overall volume- a process described as normalising- to a standardized level. 

A sample of audio files has been included in this repository for anyone interested in trying out this project. 

Credit also goes to https://github.com/jiaaro/pydub?tab=readme-ov-file for the pydub package.  

## Part 1: Deleting leading and trailing silences 🤫

The first set of code **(1-del_silence.ipynb)** deletes the leading and trailing silences in each audio file, with the silence threshold set at -40dBFS (decibels relative to full scale). The deletion of leading and trailing silences was necessary to ensure that the calculated overall dBFS  accurately reflects the word utterance portion only. 
## Part 2: Extracting metadata of each audio file 🗒️

The second set of code **(2-pre-scaling_metadata.ipynb)** extracts the metadata of each audio file and writes it to an excel sheet. This metadata is required for the calculation of the scaling factor or the amount of gain to apply to each audio file for normalisation. Metadata extracted from each audio file included the following: 

1. Bytes sample
2. Number of channels
3. Frame size 
4. RMS value
5. dBFS value
6. Peak amplitude
7. Duration in ms

## Part 3: Scaling audio files to uniform dBFS value 🔊	

This last code set **(3-scaling_audiofiles.ipynb)** scales audio files to a specified dBFS value. The metadata extracted from (2-pre-scaling_metadata.ipynb) determines the gain to be applied to each audio file. The target dBFS value for all audio files is specified at  -31.817 dBFS. 

An updated metadata of all scaled files were also created and written to an excel file. The updated metadata file includes the following details of each audio file:

1. Wavefile name
2. Bytes sample
3. Number of channels.
4. Frame size
5. RMS value
6. Scaling factor 
7. Old dBFS value
8. New dBFS value


For any questions or issues, feel free to contact Ms Jannah at nuruljannahalias@outlook.com

Thank you! 😊	
