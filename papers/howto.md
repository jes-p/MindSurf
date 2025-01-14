#Data Analysis
TestBench Manual:
"Data is stored by TestBench in a standard binary format, EDF, which is compatible with many
EEG analysis programs such as EEGLab. Following the initial information line, each successive
row in the data file corresponds to one data sample, or 1/128 second time slice of data. Successive
rows correspond to successive time slices, so for example one second of data is contained in 128
rows. Each column of the data file corresponds to to an individual sensor location or other information tag"
"Ideally you should apply a high-pass filter which matches the characteristics of the electronics
-that is, you should use a 0.16Hz first order high-pass filter to remove the background sig- nal (this also removes any longer term drift, which is not achieved by the average subtraction
method). Another method is to use an IIR filter to track the background level and subtract it - an
example is shown below in Matlab pseudocode, assuming the first row has been removed from
the array input_data():"

Matlab package: EEGLAB http://sccn.ucsd.edu/eeglab/

OpenViBE: http://openvibe.inria.fr

Emokit (Python): https://github.com/daeken/Emokit/blob/master/Announcement.md

Wiki Emotiv: http://wiki.emotiv.com/tiki-index.php?page=EmoState+And+EEG+Logger+Epoc+page

EDF format documentation: http://www.edfplus.info/

"EEG recording was conducted using Ag/AgCl electrodes mounted in a 62-channel Electro-cap (NeuroScan Inc., Eaton, OH). The ground electrode was located 10% anterior to FZ, with linked earlobes serving as references. EEG signals were recorded using a programmable DC coupled broadband SynAmps amplifier (NeuroScan, Inc., El Paso, TX). The EEG signals were amplified (gain 2500, accuracy 0.033/bit) with a recording range set to ± 55 mV in the DC to a 70-Hz frequency range. The EEG signals were digitized at 250 Hz using 16-bit analog-to-digital converters. Impedance was measured at all sites and was kept below 5 kΩ.

From the 62-channel array, EEG recording was filtered in the 2–30 Hz frequency range. The data were checked and corrected for artifacts and eye blinks were removed. The EEG recording was segmented into pieces that contained data from 30 s for encoding and 30 s for retrieval phases. The processed files were subjected to EEG power analysis (see Jaiswal et al., 2010 for details)."
http://www.sciencedirect.com/science/article/pii/S0167876014016444?via%3Dihub
