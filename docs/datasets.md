# Datasets

The analyses are based on datasets from model experiments using UKESM or its model components, such as the TerraFirma UKESM TIPMIP experiment or the CANARI HadGEM3 Large Ensemble, as well as observations and reanalyses.

You will need access to the PROMOTE group workspace (gws) to carry out your analysis and to the TerraFirma and CANARI gws to access data. Information on how to apply for those services is available in the [Get ready](get_ready.md) section.

## Model experiments
### TerraFirma UKESM TIPMIP experiment
The Terrafirma Overshoot ensemble follows the TIPMIP protocol (Jones et al., 2025), which defines a set of climate model experiments that include (i) idealised warming experiments (CO<sub>2</sub> increase only), (ii) CO<sub>2</sub> stabilisation experiments at various global warming levels and (iii) ramp-down experiments with a simulated CO<sub>2</sub> decrease (Fig. 1, Jones et al. 2025). These TIPMIP experiments have been completed with UKESM1.2.


<figure>
  <img src="images/tipmip_protocol.jpg" alt="tipmip" height="320">
  <figcaption style="text-align: left;">
<strong>Figure 1:</strong> The TIPMIP Tier 1 Earth system model (ESM) experiment protocol. ESMs are run in CO<sub>2</sub> emission mode with predicted atmospheric CO<sub>2</sub> concentration and a full carbon cycle.
</figcaption>
</figure>


<span style="font-weight: 550;">Model details</span>

* <span style="font-weight: 500;">Model:</span> UKESM1.2
* <span style="font-weight: 500;">Atmosphere:</span> UM v3.1
* <span style="font-weight: 500;">Ocean:</span> NEMO G07
* <span style="font-weight: 500;">Sea Ice:</span> SI3
* <span style="font-weight: 500;">Land:</span> JULES
* <span style="font-weight: 500;">Ice sheet:</span> BISICLES

<span style="font-weight: 550;">Data access</span>

* CMORised output is available on JASMIN at `/gws/ssde/j25b/terrafirma/TerraFIRMA/MOHC/UKESM1-2`. 
The CMORised output for each experiment is detailed [here](https://gws-access.jasmin.ac.uk/public/ukesm/TerraFIRMA/).
* Subdaily data are not available for these experiments.
* Additional experiments, e.g. for more warming levels, have been run by the TerraFIRMA project, but output is not CMORised and not available on Jasmin. Please contact Jeremy Walton (jeremy.walton@metoffice.gov.uk) or Colin Jones (colin.jones@metoffice.gov.uk) if you’d like to know more about these additional experiments and output.

### CANARI HadGEM3 Large Ensemble
The CANARI-LE (Schiemann et al., 2026) consists of 40 ensemble members of both the CMIP6 historical (1950-2014) simulation and SSP3-7.0 (2015-2100). The simulations have been completed with HadGEM3-GC1.3-MM, with the same configuration as used in CMIP6 (global configuration version 3.1).


<span style="font-weight: 650;">Model details</span>

* <span style="font-weight: 500;">Model:</span> HadGEM3-GC1.3-MM, same configuration as used in CMIP6, global configuration version 3.1
* <span style="font-weight: 500;">Atmosphere:</span> UM
* <span style="font-weight: 500;">Ocean:</span> NEMO3.6
* <span style="font-weight: 500;">Sea Ice:</span> CICE
* <span style="font-weight: 500;">Land:</span> Jules
* <span style="font-weight: 500;">Ice sheet:</span> No interactive ice sheets

<span style="font-weight: 550;">Data access</span>

* A subset of the CANARI-LE atmosphere, sea ice and ocean output variables (the [priority variables](/20240229-canari-le-priority-variables.xlsx){:download}) is available on JASMIN at `/gws/ssde/j25b/canari/shared/large-ensemble/priority`. HIST2 contains the 40 historical ensemble members over 1950-2014, SSP370 the future projection ensemble members over 2015-2100, and HIST1 are the 4 historical ensemble members which were part of CMIP6 over 1850-2014.
* Additional output variables are available on the JASMIN Elastic Tape. Please speak to Charlotte or Reinhard if you are interested in retrieving such additional data. These retrievals are slow and it is unlikely that data for the entire Large Ensemble (all members/full period) can be retrieved during the sprint week. It is however possible to retrieve data samples to start an analysis workflow or to run some tests.
* More information on the CANARI-LE and the available datasets can be found [here](https://ncas-cms.github.io/canari/).


## Observations and reanalyses

Below is a non-exhaustive list of useful observational products and reanalyses.

* <span style="font-weight: 500;">Atmosphere</span>
	* ERA5 atmosphere reanalysis
* <span style="font-weight: 500;">Greenland Ice sheet</span>
	* [MEaSUREs](https://www.earthdata.nasa.gov/about/competitive-programs/measures) program: ice sheet velocities and surface snow and ice melt
	* [MODIS](https://nsidc.org/data/modgrnld/versions/1) albedo
* <span style="font-weight: 500;">Ocean</span>
	* [HadSST](https://www.metoffice.gov.uk/hadobs/hadsst4/) dataset
	* [EN4](https://www.metoffice.gov.uk/hadobs/en4/)
	* [OSNAP](https://www.o-snap.org/data-access/) Array
	* [RAPID](https://rapid.ac.uk/data/data-download) Array
* <span style="font-weight: 500;">Biogeochemistry:</span>
	* WOA nutrients
	* ESA CCI chlorophyll and primary productivity	

If you'd like to share observational or reanalyses data that you have already downloaded, please fill this [spreadsheet](https://docs.google.com/spreadsheets/d/1zcM7b8CWcgvNZwPgc-YExNfq7xTBF59b2-m6j289Oxc/edit?usp=sharing).

## Useful files

* <span style="font-weight: 500;">Ocean:</span> the ocean the mesh_mask and subbasins files can be found in the CANARI gws at `/gws/ssde/j25b/canari/shared/large-ensemble/ocean`.
* <span style="font-weight: 500;">Ice sheet:</span> the latitude/longitude files for the ice sheet grids and the land and tile fractions and grid box area for the UM grid can be found in the PROMOTE gws at `/gws/pw/j07/promote/share/promote_analysis_sprint/useful_files`. Ice/land masks for the ice sheet grid are time dependent and can be found in the BISICLES output files.


<div style="height: 1.5em;"></div>

**^^References^^**

[1] Jones, C., et al. 2025: *The TIPMIP Earth system model experiment protocol: phase 1*. EGUsphere, (September), 1–45, [https://doi.org/10.5194/egusphere-2025-3604](https://egusphere.copernicus.org/preprints/2025/egusphere-2025-3604/). 

[2] Schiemann, R. et al. 2026: Geoscientific Model Development, submitted.
