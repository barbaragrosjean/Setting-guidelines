# Preprocess the iEEG

## Getting the data
- The NIB format
- The BIDs format

## Preprocessing Steps Overview
- Select only seeg and ecog channels
- Set the onset of the task and crop from onset to end
- Referencing
- Drop bad channels
- resample l_freq=0.1 h_freq=None
- Notch filtering
- Get the events
- Epoching
- Normalize epochs using BS normalisation
- crop the interesting event 
- resample at the correct new fs

## Detailled 
