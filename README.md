# Navigate through intracranial


## Data Structure

**Electrodes:**
- Macroelectrodes: Local field potentials (LFP), ECoG, depth EEG or SEE (generaly 8 contacts)
- Macroelectrodes: Action potentials ("spikes") and very local LFP
- Scalpe electrodes

**Terminology:** \
_ hemisphere: L or R \
___ region code \
__ recoding site number \

| Label         | Region                       |
| ------------- | ---------------------------- |
| **HPC / HIP** | Hippocampus                  |
| **AH / aH**   | Anterior hippocampus         |
| **PH / pH**   | Posterior hippocampus        |
| **AMY / AMG** | Amygdala                     |
| **EC**        | Entorhinal cortex            |
| **PHC**       | Parahippocampal cortex       |
| **MTG**       | Middle temporal gyrus        |
| **STG**       | Superior temporal gyrus      |
| **ITG**       | Inferior temporal gyrus      |
| **TP**        | Temporal pole                |
| **FG**        | Fusiform gyrus               |
| **SFG**       | Superior frontal gyrus       |
| **MFG**       | Middle frontal gyrus         |
| **IFG**       | Inferior frontal gyrus       |
| **OFC**       | Orbitofrontal cortex         |
| **ACC**       | Anterior cingulate cortex    |
| **PCC**       | Posterior cingulate cortex   |
| **MCC**       | Middle cingulate cortex      |
| **SMA**       | Supplementary motor area     |
| **M1**        | Primary motor cortex         |
| **S1**        | Primary somatosensory cortex |
| **PC**        | Precuneus                    |
| **PPC**       | Posterior parietal cortex    |
| **IPL**       | Inferior parietal lobule     |
| **SPL**       | Superior parietal lobule     |
| **OCC**       | Occipital cortex             |
| **V1**        | Primary visual cortex        |
| **V2**        | Secondary visual cortex      |
| **Ins**       | Insula                       |
| **Thal**      | Thalamus                     |
| **Caud**      | Caudate                      |
| **Put**       | Putamen                      |
| **GP**        | Globus pallidus              |
| **NAcc**      | Nucleus accumbens            |


---> Check the Channel name file (.txt) to have the oroginal terminology.


**NCS** \

.ncs files contains the data for each contact electrodes. In the header: 
- Actual name withe the terminology
- Volt scaler: to multiply to the data to get the unit in volt
- Reference electrodes and if it has changed
- sampling rate 
- ...

- About the time. after participant 65, use UTC time. but before has a reference time 

Important to know if the ncs file is not complet the header of the data package would be < 512 bytes. And the actual not complete data is a copy of the next package. 


## Tasks
There is a .nev file with the events.


