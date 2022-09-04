# BBH Merger GW Data

## [Credits: [PyCBC](https://pycbc.org/pycbc/latest/html/index.html), [LAL](https://lscsoft.docs.ligo.org/lalsuite/), [LIGO Scientific Collaboration](https://www.ligo.org/), [Virgo Scientific Collaboration](http://public.virgo-gw.eu/the-virgo-collaboration/)]

### This repository contains

- **simulated** noisy BBH merger GW signals for neural network training
- and **detector waveforms** from LIGO’s event catalogues.
    - [Hanford Detector](https://en.wikipedia.org/wiki/LIGO#Observatories) Label: H1
    - [Livingston Detector](https://en.wikipedia.org/wiki/LIGO#Observatories) Label: L1
    - [Virgo Detector](https://en.wikipedia.org/wiki/Virgo_interferometer) Label: V1

The **goal** of this repository is to provide everyone (and myself) with **easy-to-access BBH merger GW data** since waveform simulation and LIGO merger event catalogue access do require special software packages and certain operating systems.

### Simulated Signal

- Data Specifications
    
    Waveform Model: `[IMRPhenomD](https://lscsoft.docs.ligo.org/lalsuite/lalsimulation/group___l_a_l_sim_i_m_r_phenom__c.html)`
    
    Noise Model: [aLIGO zero-detuned Frequency-domain Noise Model](https://pycbc.org/pycbc/latest/html/pycbc.psd.html#pycbc.psd.analytical.aLIGOZeroDetHighPower)
    
    Sampling Frequency: 2048 Hz
    
    Duration: 6 s
    
    Individual Mass Range: 1 - 100 Solar Masses
    
    Merger Position (Random): 
    
    - ~ first 2 s of the 6 s waveform: label → 0
    - ~ 3 s of the 6 s waveform: label → 1
    - ~ last 2 s of the 6 s waveform: label → 2
    
    Luminosity Distance (Random): 410 Mpc, 610 Mpc, or 810 Mpc 
    
    Normal Strain Amplitude: 10e-22 to 10e-21
    
    Normal Noise Amplitude: 10e-22
    

### Detector Merger Events (see catalogue names for more information)

- Data Specifications:
    
    Duration: ~32 s
    
    Sampling Frequency: 4096 Hz
    
- Event Access Log (What’s not included in this repository)
    
    ```html
    past_gw_detection_catalogue.py
    ############## log ###########################################
    Access time: 2022-09-03 21:11:34.146502
    Catalogue: GWTC-1-confident
    11 events.Error... Skipping...GW150914-v3
    Error... Skipping...GW151012-v3
    Error... Skipping...GW151226-v2
    Error... Skipping...GW170104-v2
    Error... Skipping...GW170608-v3
    Error... Skipping...GW170823-v1
    Event accessed: 5
    GWTC-1-confident time: 4.164625883102417
    #############################
    Access time: 2022-09-03 21:11:38.312371
    Catalogue: GWTC-1-marginal
    14 events.Error... Skipping...151008-v1
    Error... Skipping...151012.2-v1
    Error... Skipping...151116-v1
    Error... Skipping...161202-v1
    Error... Skipping...161217-v1
    Error... Skipping...170208-v1
    Error... Skipping...170219-v1
    Error... Skipping...170405-v1
    Error... Skipping...170412-v1
    Error... Skipping...170423-v1
    Error... Skipping...170616-v1
    Error... Skipping...170630-v1
    Error... Skipping...170705-v1
    Error... Skipping...170720-v1
    Event accessed: 0
    GWTC-1-marginal time: 1.2506000995635986
    #############################
    Access time: 2022-09-03 21:11:39.563754
    Catalogue: Initial_LIGO_Virgo
    2 events.Error... Skipping...GRB051103-v1
    Error... Skipping...blind_injection-v1
    Event accessed: 0
    Initial_LIGO_Virgo time: 0.0004360675811767578
    #############################
    Access time: 2022-09-03 21:11:39.565012
    Catalogue: O1_O2-Preliminary
    12 events.Error... Skipping...GW150914-v1
    Error... Skipping...GW150914-v2
    Error... Skipping...GW151012-v1
    Error... Skipping...GW151012-v2
    Error... Skipping...GW151226-v1
    Error... Skipping...GW170104-v1
    Error... Skipping...GW170608-v1
    Error... Skipping...GW170608-v2
    Error... Skipping...GW170814-v1
    Error... Skipping...GW170814-v2
    Error... Skipping...GW170817-v1
    Error... Skipping...GW170817-v2
    Event accessed: 0
    O1_O2-Preliminary time: 0.013202905654907227
    #############################
    Access time: 2022-09-03 21:11:39.579094
    Catalogue: O3_Discovery_Papers
    8 events.Error... Skipping...GW190425-v1
    Error... Skipping...GW200105-v1
    Event accessed: 6
    O3_Discovery_Papers time: 4.199512004852295
    #############################
    Access time: 2022-09-03 21:11:43.781673
    Catalogue: GWTC-2
    39 events.Error... Skipping...GW190421_213856-v1
    Error... Skipping...GW190424_180648-v1
    Error... Skipping...GW190425-v2
    Error... Skipping...GW190514_065416-v1
    Error... Skipping...GW190521_074359-v1
    Error... Skipping...GW190527_092055-v1
    Error... Skipping...GW190620_030421-v1
    Error... Skipping...GW190630_185205-v1
    Error... Skipping...GW190707_093326-v1
    Error... Skipping...GW190708_232457-v1
    Error... Skipping...GW190719_215514-v1
    Error... Skipping...GW190731_140936-v1
    Error... Skipping...GW190909_114149-v1
    Error... Skipping...GW190910_112807-v1
    Error... Skipping...GW190930_133541-v1
    Event accessed: 24
    GWTC-2 time: 17.660564184188843
    #############################
    Access time: 2022-09-03 21:12:01.445160
    Catalogue: GWTC-2.1-confident
    44 events.Error... Skipping...GW190403_051519-v1
    Error... Skipping...GW190413_052954-v2
    Error... Skipping...GW190421_213856-v2
    Error... Skipping...GW190425_081805-v3
    Error... Skipping...GW190426_190642-v1
    Error... Skipping...GW190514_065416-v2
    Error... Skipping...GW190521_074359-v2
    Error... Skipping...GW190527_092055-v2
    Error... Skipping...GW190620_030421-v2
    Error... Skipping...GW190630_185205-v2
    Error... Skipping...GW190707_093326-v2
    Error... Skipping...GW190708_232457-v2
    Error... Skipping...GW190719_215514-v2
    Error... Skipping...GW190731_140936-v2
    Error... Skipping...GW190805_211137-v1
    Error... Skipping...GW190910_112807-v2
    Error... Skipping...GW190925_232845-v1
    Error... Skipping...GW190930_133541-v2
    Event accessed: 26
    GWTC-2.1-confident time: 19.13411784172058
    #############################
    Access time: 2022-09-03 21:12:20.580502
    Catalogue: GWTC-2.1-marginal
    2 events.Event accessed: 2
    GWTC-2.1-marginal time: 1.3868541717529297
    #############################
    Access time: 2022-09-03 21:12:21.971501
    Catalogue: GWTC-3-confident
    35 events.Error... Skipping...GW191103_012549-v1
    Error... Skipping...GW191109_010717-v1
    Error... Skipping...GW191126_115259-v1
    Error... Skipping...GW191129_134029-v1
    Error... Skipping...GW191204_110529-v1
    Error... Skipping...GW191204_171526-v1
    Error... Skipping...GW191216_213338-v1
    Error... Skipping...GW191222_033537-v1
    Error... Skipping...GW200112_155838-v1
    Error... Skipping...GW200128_022011-v1
    Error... Skipping...GW200220_124850-v1
    Error... Skipping...GW200225_060421-v1
    Error... Skipping...GW200302_015811-v1
    Error... Skipping...GW200306_093714-v1
    Event accessed: 21
    GWTC-3-confident time: 15.557221174240112
    #############################
    Access time: 2022-09-03 21:12:37.530404
    Catalogue: GWTC-3-marginal
    7 events.Error... Skipping...191118_212859-v1
    Error... Skipping...200121_031748-v1
    Error... Skipping...200214_224526-v2
    Error... Skipping...200311_103121-v1
    Error... Skipping...GW200105_162426-v2
    Event accessed: 2
    GWTC-3-marginal time: 1.6110539436340332
    ```
    

### Accessing Data Files

1. HarvardDV (for archive)
2. GitHub Direct Access
    
    **URL convention:** ‘`https://raw.githubusercontent.com/xli2522/BBH-merger-waveform-data-release/blob/main/GWTC-2/csv_data/GW190408_181802-v1-1238782700.3-L1.csv`’
    
    ```html
    C**onvention**:  /main/catalogue-name/csv_data/event_name        -GPStime     -detector.csv
    **Example**:     /main/GWTC-2        /csv_data/GW190408_181802-v1-1238782700.3-L1      .csv
    ```
    

### Other resources:

GPS Time Conversion: 

[https://www.andrews.edu/~tzs/timeconv/timeconvert.php](https://www.andrews.edu/~tzs/timeconv/timeconvert.php)