# ATP_pulse_analysis

Disclaimer: most of these functions were written for a single purpose rather than to be widely applicable. Therefore in some cases they require a specific file structure/layout and may need minor modifications to be applied to other projects.

> These macros and scripts were first written for  
> Human iPSC-derived Down syndrome astrocytes display genome-wide perturbations in gene expression, an altered adhesion profile, and increased cellular dynamics; *Human Molecular Genetics, Volume 29, Issue 5, 1 March 2020* Blandine Ponroy Bally,  W Todd Farmer,  Emma V Jones,  Selin Jessa, J Benjamin Kacerovsky,  Alexandre Mayran,  Huashan Peng,  Julie L Lefebvre, Jacques Drouin,  Arnold Hayer,  Carl Ernst,  Keith K Murai

Versions in this repo may contain changes, modifications and bug fixes since the original publication. For scripts as used for the publication see [Ponroy2020_HMG/ATP_pulse_analysis/](https://github.com/murailab/Ponroy2020_HMG/tree/master/ATP_pulse_analysis)
 
open_save_n_channels.ijm re-saves all image files (with user specified file ending) in a folder as .tif images into a specified directory

ATP_pulse_macro.ijm extracts F/F0 time traces in user defined ROIs and saves them as .cv files

"Ca_pulse_analyzer_v2_171219.R" and "base_analyzer_180125.R" analyse the traces (from the above csv files) and extract summary statistics: 
- n_resp/perc_resp = number/percentage responding cells (traces that cross the user difined activity threshold during analyzed time frame (ATP pulse or base line))  
- n_filtered = number of cells excluded from analysis for being active during baseline
- mean_amp_all/sd_amp_all = mean amplitude/sd for all analyzed cells (excluding filtered) 
- mean_amp_resp/sd_amp_resp = mean amplitude/sd for reesponders only
- mean_AUC/sd_AUC = mean area under the curve/sd

For "Ca_pulse_analyzer_v2_171219.R" and "base_analyzer_180125.R" to run the functions file "functions_for_ca_analyzer.R" needs to be read in first. 

Frames to be analyzed, filter thresholds and activity threshold havee to be specifed by the user in the first lines of the script

