# Banerjee et al. 2021 - Miniature Neurotransmission and ageing of Drosophila
 
 Produced for and by the McCabe Laboratory at EPFL - https://mccabelab.org 
 
--- Custom Macros employed for Adult Neuromuscular Junction morphometric analysis --- 

---  Active_Zone_Counts_2021.ijm ---
For AZs -Macro for folder processing of confocal images consisting of:
 * - Green: adult presynaptic terminals
 * - Red: Active Zones (NC82 staining)
 * - Blue: Anti-vGlut staining
 *
 *In short this macro
 * - Segments the active zones as single points using a lacal maximum finder on the red channel
 * - Segments the terminal and vGlut channels using a threshold to localize the regions of interest
 * - Counts the number of active zones inside the regions of interest
 *
 * Output:
 * - A results table with one row per image and the count of AZs in each zone.
 *
 * Requirements:
 * - PTBIOP Update Site https://imagej.net/update-sites/followinghttps://imagej.net/update-sites/following
 *
 * Code by Olivier Burri, EPFL - SV - PTECH - BIOP
 * For Dr. Soumya Banerjee, EPFL - SV - UPMCCABE
 
 
 --- Measure_Presynaptic_Terminal_Areas_2021 ---
 For Presynaptic area-Measurements of adult NMJ presynaptic terminals area during ageing
 *
 * This macro expects a single channel image of adult terminals.
 *
 * It will measure an area based on auto-thresholding on the adult synapse channel which will have been
 * - Background subtracted to remove low frequency local structures
 * - Smoothed with a 3x3 gaussian kernel
 * - Intensity variations dampened by means of applying a square root.
 *
 * This works under the assumptions that the background does not change between conditions
 * and that the changes in area are not expected to be major (less than 3x fold change). Otherwise another measure might be necessary
 *
 * Careful with absolute area measurements. Area ratios, with respect to
 * a known measurable structure is usually much more informative.
 *
 * OUTPUT:
 * A results table with the area of all particles above 0.4 um^2 on the image
 *
 * Code by Olivier Burri, EPFL - SV - PTECH - BIOP
 * For Dr. Soumya Banerjee, EPFL - SV - UPMCCABE
 *
 * Last modified: 07.06.2021
 
 --  EasyXT_Size_And_Intensity_Of_Synaptic_Proteins_In_Imaris.groovy --
 
 --- FOR INTENSITY and SIZE-Detect Surfaces and Spots in adult drosophila NMJ terminals in Imaris using EasyXT ---
 * Filter spots wether they are inside the surface or not
 * Export the volumes of the spots as results
 * NOTE: This has been optimized on deconvolved images and may not be as accurate on raw data
 *
 * Requirements
 * ------------
 * The following update sites need to be enabled
 * 1. EasyXT-Fiji, https://biop.epfl.ch/Fiji-EasyXT/
 * 2. 3D ImageJ Suite
 *
 * A Working Imaris Instance running version 9.5 (or above) is required
 * with a valid XTensions license
 *
 * Imaris should be open before starting this code.
 * BUG: Make sure that Imaris is open AND that a dataset is loaded before starting.
 * It is a known issue that opening an image from EasyXT on a fresh Imaris can cause a crash.
 *
 * Author: Olivier Burri, EPFL - SV - PTECH - BIOP
 * For: Dr. Soumya Banerjee, EPFL - SV - UPMCCABE
 * February 4th 2021
 *
 * Last modified: June 7th 2021
 
 
 
 