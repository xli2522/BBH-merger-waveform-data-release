# BBH Merger GW Data

## [Credits: [PyCBC](https://pycbc.org/pycbc/latest/html/index.html), [LAL](https://lscsoft.docs.ligo.org/lalsuite/), [LIGO Scientific Collaboration](https://www.ligo.org/), [Virgo Scientific Collaboration](http://public.virgo-gw.eu/the-virgo-collaboration/)]

Picture (Virgo Detector): [http://public.virgo-gw.eu/wp-content/uploads/2019/12/AdVirgo-300dpi-scaled.jpg](http://public.virgo-gw.eu/wp-content/uploads/2019/12/AdVirgo-300dpi-scaled.jpg)

### This repository contains

- **simulated** noisy BBH merger GW signals for neural network training
- and **detector waveforms** from LIGO’s event catalogues.
    - [Hanford Detector](https://en.wikipedia.org/wiki/LIGO#Observatories) Label: H
    - [Livingston Detector](https://en.wikipedia.org/wiki/LIGO#Observatories) Label: L
    - [Virgo Detector](https://en.wikipedia.org/wiki/Virgo_interferometer) Label: V

***Goals of this repository:***

- provide **datasets** that were used in our projects so anyone can try to reproduce our results.
- provide **easy-to-access BBH merger GW data** since waveform simulation and LIGO merger event catalogue access do require special software packages and certain operating systems.

### Simulated Signal

- Data Specifications
    
    Waveform Model: `[IMRPhenomD](https://lscsoft.docs.ligo.org/lalsuite/lalsimulation/group___l_a_l_sim_i_m_r_phenom__c.html)`
    
    Noise Model: [aLIGO zero-detuned Frequency-domain Noise Model](https://pycbc.org/pycbc/latest/html/pycbc.psd.html#pycbc.psd.analytical.aLIGOZeroDetHighPower)
    
    Sampling Frequency: 2048 Hz
    
    Duration: 6 s
    
    File Type: **CSV** ([GitHub](https://github.com/xli2522/BBH-merger-waveform-data-release)) and **Pickle** ([Harvard DV](https://doi.org/10.7910/DVN/QFCBCL)); in **Pandas dataframe**
    
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
    
    Duration: 32 s (longer durations available; create a Github request)
    
    Sampling Frequency: 4096 Hz and 16384 Hz
    
    File Type: **GWF**, **HDF5**, and **Compressed TXT** (TXT.GZ) for each event
    
- Event Access Log
    
    NOTE: detector label error, will fix soon
    
    NOTE: detector label fixed [220911]
    
    ```html
    past_gw_detection_catalogue.py
    ############## log ##############
    	xli2522@github.com
    #############################
    Access time: 2022-09-11 21:29:35.971644
    Catalogue: GWTC-1-confident
    11 events.Event accessed: 11
    GWTC-1-confident time: 399.68413186073303
    #############################
    Access time: 2022-09-11 21:36:15.657745
    Catalogue: GWTC-1-marginal
    14 events.Event accessed: 14
    GWTC-1-marginal time: 356.59337401390076
    #############################
    Access time: 2022-09-11 21:42:12.252461
    Catalogue: Initial_LIGO_Virgo
    2 events.Event accessed: 2
    Initial_LIGO_Virgo time: 2.1457672119140625e-06
    #############################
    Access time: 2022-09-11 21:42:12.253374
    Catalogue: O1_O2-Preliminary
    12 events.Event accessed: 12
    O1_O2-Preliminary time: 303.4168529510498
    #############################
    Access time: 2022-09-11 21:47:15.671878
    Catalogue: O3_Discovery_Papers
    8 events.Event accessed: 8
    O3_Discovery_Papers time: 293.9747130870819
    #############################
    Access time: 2022-09-11 21:52:09.650279
    Catalogue: GWTC-2
    39 events.Event accessed: 39
    GWTC-2 time: 1298.7019248008728
    #############################
    Access time: 2022-09-11 22:13:48.356191
    Catalogue: GWTC-2.1-confident
    44 events.Event accessed: 44
    GWTC-2.1-confident time: 1486.8560099601746
    #############################
    Access time: 2022-09-11 22:38:35.214129
    Catalogue: GWTC-2.1-marginal
    2 events.Event accessed: 2
    GWTC-2.1-marginal time: 91.25677800178528
    #############################
    Access time: 2022-09-11 22:40:06.474245
    Catalogue: GWTC-3-confident
    35 events.Event accessed: 35
    GWTC-3-confident time: 1294.0056397914886
    #############################
    Access time: 2022-09-11 23:01:40.482119
    Catalogue: GWTC-3-marginal
    7 events.Event accessed: 7
    GWTC-3-marginal time: 335.6260190010071
    ```
    

### Accessing Data Files

1. HarvardDV (for archive)
2. GitHub Direct Access
    
    **URL convention:** ‘`https://raw.githubusercontent.com/xli2522/BBH-merger-waveform-data-release/blob/main/GWTC-2/csv_data/GW190408_181802-v1-1238782700.3-L1.csv`’
    
    ```html
    **Convention 1**:  /main/catalogue-name/csv_data/event_name        -GPStime     -detector.csv
    **Example 1**:     /main/GWTC-2        /csv_data/GW190408_181802-v1-1238782700.3-L1      .csv
    **Convention 2**:  /main/catalogue-name  /event_name /file_name
    **Example 2**:     /main/GWTC-1-confident/GW150914-v3/H-H1_GWOSC_16KHZ_R1-1126259447-32.txt.gz
    ```
    

### Other resources:

GPS Time Conversion: 

[https://www.andrews.edu/~tzs/timeconv/timeconvert.php](https://www.andrews.edu/~tzs/timeconv/timeconvert.php)

[https://www.ligo.org/science/Publication-O2BBHPop/index.php#:~:text=The%20BBH%20Mass%20Spectrum&text=The%20%22standard%22%20mass%20distribution%20is,probability%20decreases%20with%20increasing%20mass).](https://www.ligo.org/science/Publication-O2BBHPop/index.php#:~:text=The%20BBH%20Mass%20Spectrum&text=The%20%22standard%22%20mass%20distribution%20is,probability%20decreases%20with%20increasing%20mass).)
