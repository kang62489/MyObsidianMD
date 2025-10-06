---
Established: 2024-12-02
Last Updated: 2025-03-09
Description: While designing patch clamp + ACh imaging experiments, I was wondering if current sampling rates (20 Hz, 50 ms) can actually record a single release event. Therefore I did some short survey and analysis
---
# MEMO
1. The fastest sampling rates of the CCD camera (PCO.Panda) according to the manual are 40 fps = 25 ms (@full size: 2048 x 2048 (~230 um x ~230 um))
	1. I'm using 1024 x 1024, maybe can be faster (2X)? Because each line is around 12.5 us, current minimum speed may be 12.5 us x 1024 lines ~= 12.5 ms = 80 fps
2. The average periods of ACh releases which measured in Matityahu et al's supplemental info are 0.78 s. The measurement was done on fig2b, and results are saved in a CSV file (periods_of_release_in_Matityahu_sup_info_fig2b.csv). The tool used in the measurement are image J (Fiji).
3. Since I got some responses shapes like ACh spontaneous releases, I then used the ROI referred to the sup info (30 um x 30 um) measure the corrected image stacks (Corr_20241011-0030.tif)
	1. The csv file (releases_in_20241011-0030.csv) is the results, just for recording.
	2. The measurement of periods were also done in imageJ (results: periods_of_release_in_corr_20241011.csv). The results shows that there are several periods closed to 780 ms (e.g. 600, 720 ms). However, the signals contains releases from multiple CINs
	3. ![](<ROI_30um_x63y96_Corr_20241011.jpg>)

# Folder Structure (0 directories, 7 files)
RN_001
├── Corr_20241011-0030.tif
├── Matityahu_2023_supinfo_fig2b.jpg
├── periods_of_release_in_corr_20241011.csv
├── periods_of_release_in_Matityahu_sup_info_fig2b.csv
├── releases_in_20241011-0030.csv
├── RN_001_index.md
└── ROI_30um_x63y96_Corr_20241011.jpg

