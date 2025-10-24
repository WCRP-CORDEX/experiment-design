---
pdf: true
---

# CORDEX experiment design for dynamical downscaling of CMIP6

**28 Apr 2025**

DOI: [10.5281/zenodo.15268192](https://doi.org/10.5281/zenodo.15268192)

The COordinated Regional climate Downscaling EXperiment ([CORDEX](http://cordex.org)) was implemented under the auspices of the World Climate Research Program ([WCRP](http://www.wcrp-climate.org)).
Its aim is to improve downscaling techniques and their use in understanding and assessing regional climate change.
It also provides robust regional climate information for application in vulnerability, impacts, and adaptation (VIA) studies.
The CORDEX activity based on the downscaling of global projections from the fifth phase of the Climate Model Intercomparison Project ([CMIP5](https://wcrp-cmip.org/cmip-phases/cmip5)) has been ongoing since 2010 ([CORDEX experiment design for dynamical downscaling of CMIP5](https://doi.org/10.5281/zenodo.15199425)) and soon comes to its end.
This experiment design document presents a simulation framework for the dynamical downscaling of global climate projections from the sixth phase of CMIP ([CMIP6](http://www.wcrp-climate.org/wgcm-cmip/wgcm-cmip6)).
The general aim is to downscale a subset of climate scenarios from the CMIP6 ensemble of projections generated in [ScenarioMIP](https://wcrp-cmip.org/mips/scenariomip), and to make these downscaled regional scenarios publicly available.
For more details see [Gutowski et al. 2016](https://www.geosci-model-dev.net/9/4087/2016/) and the [CORDEX White paper](https://cordex.org/wp-content/uploads/2021/05/The-future-of-CORDEX-MAY-17-2021-1.pdf).

In addition to the continental-scale downscaling addressed in this document, CORDEX includes many other components.
For example, [the Flagship Pilot Studies](https://cordex.org/strategic-activities/flagship-pilot-studies) (FPS) and regional workshops for climate and VIA communities.
CORDEX is a continuous activity that is not divided into phases (1st, 2nd, etc.) and not necessarily related to the CMIP cycles.
The framework described in this document is simply referred to as CORDEX-CMIP6.
Newer versions of this document may exist.
Find the latest one at: [https://doi.org/10.5281/zenodo.15199301](https://doi.org/10.5281/zenodo.15199301).

## 1. CORDEX domains

The requirement of a common domain is fundamental to coordination of activities that produce common output datasets and facilitate ease of analysis of results for given domains.
[14 standard continental-scale CORDEX domains](http://cordex.org/domains/) have received an official CORDEX designation and include: South America, Central America, North America, Europe, Mediterranean, Middle East and North Africa, Africa, Central Asia, South Asia, East Asia, Southeast Asia, Australasia, the Arctic and Antarctica.
The simulations have to follow the size specifications for the CORDEX domains[^1], paying particular attention to the specified minimum domain sizes.
Notably, the CORDEX domain has to be fully inside your model domain and not include any of the boundary relaxation zones.
It is appreciated that domains will not be identical, as for various reasons groups may choose to modify their actual domains somewhat.

This experiment design addresses the 14 continental-scale CORDEX domains, which cover the majority of the populated land areas worldwide, as well as the Arctic and Antarctic.
Currently, smaller domains may be addressed within [the Flagship Pilot Studies](https://cordex.org/strategic-activities/flagship-pilot-studies) (FPS) programme.

If the regional CORDEX communities think that the configuration of their CORDEX domains is not optimal (e.g. too small, too large, etc.) they can provide a formal request to [the International Project Office for CORDEX](https://cordex.org/about/project-office/) (IPOC) to update the current configuration.
It is also possible to apply for a new CORDEX domain (see [Criteria for Selecting and Updating CORDEX Domains](https://cordex.org/wp-content/uploads/2020/09/Domain-Criteria-Document-FINAL.pdf)).
The request for updating a CORDEX domain has to come from [the Point-of-Contact](https://cordex.org/about/points-of-contact/) (POC) of a CORDEX domain, after a common agreement has been reached, not from individual RCM groups.
It is recognised that any choice of a domain may not be optimal for all groups.

Similar to [the CORDEX experiment design for the dynamical downscaling of CMIP5](https://doi.org/10.5281/zenodo.15199425), the CORDEX-Africa domain is a focus region.
We would therefore like to remind you to prioritize the Africa domain when selecting regions for integration beyond your ‘home domain’.

## 2. Resolution/Grid-spacing

In order to provide an advancement compared to the previous CORDEX simulations, and to resolve additional features of regional climate, the grid-spacing of the new CORDEX simulations ideally should be on the order of a few tens-of-kilometers.
However, a flexible choice of grid-spacing between different domains is allowed, to accommodate the needs and capacities of different communities and groups.

The primary targets are grid-spacings of 25 km and 12.5 km.
The regional CORDEX communities should decide which resolution they need and can afford, with a preference for higher resolutions when possible.
The POCs for each domain should provide guidance on the preferred resolutions for their domain.

It is recommended that one common grid-spacing be used per domain to avoid a wide range of resolutions for the same domain.
A resolution between 25 and 12.5 km may also be used if both 25 and 12.5 km are not optimal, and if there is a common agreement on an intermediate resolution within a domain.
Resolutions higher than 12.5 km may also be used upon agreement within a domain.
However, it is recommended that corresponding, complementary simulations at the domain’s primary, coarser resolution also be provided.

## 3. Model complexity

As with previous CORDEX simulations, dynamical downscaling for CMIP6 should be done, at a minimum, with regional atmosphere-land surface models.
However, increased efforts towards regional earth system models (RESMs), which include additional model components to represent other processes (e.g. ocean, sea ice, snow, urban, lakes, vegetation/agriculture, land hydrology, glaciers, aerosols and chemistry), are encouraged.
When possible, models should also be run in the atmosphere-land only configuration, as well as with one, or more, additional component models, in order to document the impact of the additional processes on regional climate.
As far as is practical, each domain should also strive for a subset of simulations that use multiple models representing the same component processes to provide a multi-model perspective on RESM simulations.
Output and archiving of additional variables from RESMs, beyond the standard CORDEX variables, should be coordinated by each regional domain in consultation with [the CORDEX Science Advisory Team](https://cordex.org/about/science-adv-team/) (SAT).
Many RCM details are model specific (e.g., the number of vertical levels and top level), so it is up to the RCM groups to define an optimal configuration for their RCMs.
Multiple nesting can be used when necessary.
If multiple nesting is used, the targeted domain size and resolution should still follow the standards established for that domain.
Consult with the domain's POCs on this.

Variable resolution global climate models (VR-GCMs) that follow the CORDEX protocol for a given domain (e.g., resolution, etc.) may also contribute to that domain.
In this case, the use of atmospheric nudging to incorporate information from the driving GCMs’ atmosphere is encouraged; thus, making the VR-GCMs more comparable to the limited area RCMs.
The inclusion of VR-GCMs adds to the overall diversity of the CORDEX ensembles, which provides some advantages, but the methodological differences when compared to limited area RCMs should be considered when combining the VR-GCMs and RCMs in an ensemble.
There are many ways that variable resolution is achieved and it is up to the modelling groups to determine an optimal configuration.

## 4. Evaluation experiment

All groups must first carry out an evaluation simulation driven by the ERA5 reanalysis for each domain they simulate.
The ERA5 reanalysis covers 1979-2024 (2024 = last full year, as of April 2025), and the evaluation experiment must cover at least the 1979-2020 period, or a longer period depending on the availability of the ERA5 forcing.
Model level or pressure level data may be used to drive RCMs.
A one year spin-up (1979) is recommended for atmosphere-land models, but a longer spin-up (or an offline spin-up) may be required for models that include additional climate system components.

The ERA5 reanalysis has [a pronounced cold bias in lower stratospheric temperature](https://www.ecmwf.int/en/elibrary/19362-global-stratospheric-temperature-bias-and-other-stratospheric-aspects-era5-and) for the years from 2000 to 2006.
In order to fix this problem, a new set of the ERA5 reanalysis, termed ERA5.1, has been produced for 2000-2006.
The impact of the cold bias on downscaling is not clear but it may potentially affect RCM simulations.
It is recommended that the corrected version, ERA5.1, be used for 2000-2006.

Additional evaluation experiments (e.g. at different resolutions and/or driven by other reanalyses) may also be carried out to complement the ERA5-driven experiment.
It is up to the regional CORDEX communities to set up their own experiment design for such additional reanalysis-driven simulations, depending on their own resources and scientific questions.

It is recommended that prescribed sea surface temperature and sea ice fraction also be obtained from the driving reanalyses.
The driving reanalyses should be used at 3-hourly update frequency and at their native resolution when possible.

### GHG forcing

Through 2014, RCM groups should use the same historical atmospheric greenhouse gas (GHG) forcing as in CMIP6.
For periods starting from 2015 onwards (e.g. 2015-2020) it is recommended that the scenario GHG forcing for the SSP3-7.0 be used.
The global and annual-mean time series of GHG concentrations for both the historical and scenario periods are available from [the input4MIPs database](https://esgf-node.llnl.gov/projects/input4mips/).
See for more details [Meinshausen et al. 2017](https://doi.org/10.5194/gmd-10-2057-2017) and [Meinshausen et al. 2019](https://doi.org/10.5194/gmd-2019-222).

### Land use/Land cover

As the first step, it is recommended that the static land cover and land use maps that are a regional model’s default be used.
Recommendations for the implementation of transient land use change (e.g., datasets, translation to RCMs, etc.) will be provided later.
When the recommendations become available, simulations with the static land cover and land use may be complemented by a number of new simulations with the transient land use change.

### Aerosol

A static aerosol dataset (e.g. a regional model’s default climatology) is considered as a minimum requirement.
It is strongly encouraged that for the evaluation experiment, RCM groups apply up-to-date regional or global aerosol datasets with realistic variability in time (monthly variation and trend) and space.
For example, the state-of-the-art monthly mean MERRA-2 aerosol dataset can be used.
Implementation of aerosol forcing in RCMs is model-dependent and general recommendations and more details are provided through [a dedicated document](https://cordex.org/wp-content/uploads/2021/02/aerosol4cordex.pdf) which will be regularly updated.
Comments and questions can be directly posted in [a living document](https://tinyurl.com/aerosol4cordex) or sent to the IPOC.

### Spectral nudging

It is up to RCM groups to decide on whether to apply large-scale spectral nudging for the reanalysis driven experiment or not.
Specific details of the spectral nudging (e.g. strength, scales, variables, and levels) can be strongly region-dependent (e.g. the midlatitudes or tropics), so it is also up to RCM groups to decide on parameters for the nudging, based on their regional expertise.
When possible, it is recommended that RCM groups provide two reanalysis-driven evaluation simulations - with and without nudging.

## 5. Historical experiment

Boundary conditions from the CMIP6 historical experiment, requested by CORDEX, are available for 1950-2014[^2].
In addition to the moving 30-yr reference period (1991-2020 for the 2021-2030 decade) the World Meteorological Organisation ([WMO](https://public.wmo.int/en)) has also recommended that [1961-1990 be used as a standard static reference period](https://wmoomm.sharepoint.com/:b:/r/sites/wmocpdb/eve_activityarea/Climate%20Data%20and%20Monitoring_905e0e2b-3eb4-e911-a967-000d3a442d3c/WWR/clino/16953-2021-S-CS-CMP-CLINO9120-en.pdf?csf=1&web=1&e=cD4Ib7) for long-term climate change assessments.
The CORDEX historical simulations have to cover at least 1960-2014 or preferably the entire 1950-2014 period.
A one year spin-up (1950 or 1960) is recommended for atmosphere-land models but a longer spin-up (or, e.g., an offline spin-up) may be required for models that include additional climate system components.

### GHG forcing

RCM groups should use the same historical GHG forcing as in the driving CMIP6 models.
See for more details [Meinshausen et al. 2017](https://doi.org/10.5194/gmd-10-2057-2017).

### Land use/Land cover

As the first step, it is recommended that the static land cover and land use maps that are a regional model’s default be used.
Recommendations for the implementation of a transient land use change (e.g., datasets, translation to RCMs, etc.) will be provided later.
When the recommendations become available, simulations with the static land cover and land use may be complemented by a number of new simulations with the transient land use change.

### Aerosol

A static aerosol dataset (e.g., a regional model’s default climatology) is considered as a minimum requirement.
It is strongly encouraged that for the historical experiment RCM groups apply aerosol forcing which is either directly consistent with the driving CMIP6 GCMs or more broadly consistent with the CMIP6 aerosol forcing.
The first priority is given to aerosol optical properties (e.g., total aerosol optical depth or aerosol optical depth per species) provided by most CMIP6 GCMs.
General recommendations and more details are provided through [a dedicated document](https://cordex.org/wp-content/uploads/2021/02/aerosol4cordex.pdf) which will be regularly updated.
Comments and questions can be directly posted in [a living document](https://tinyurl.com/aerosol4cordex) or sent to the IPOC.

### Spectral nudging

It is up to RCM groups to decide on whether to apply large-scale spectral nudging for the CMIP6 driven simulations or not.

## 6. Scenario experiment

Boundary conditions from the CMIP6 ScenarioMIP, requested by CORDEX, are available for 2015-2100.
The main focus in [the CORDEX Request to CMIP6](https://cordex.org/experiment-guidelines/cordex-cmip6/requests-to-cmip6/) (2016) was on the Tier 1 SSP5-8.5 and SSP1-2.6 scenarios.
However, currently, there is a stronger focus on the SSP3-7.0 as a high impact scenario instead of the SSP5-8.5.
Thus, the SSP3-7.0 and SSP1-2.6 scenarios have to be downscaled first for one ensemble member for the entire 2015-2100 period.
It is also recommended that additional downscaling using the SSP2-4.5 scenario and/or the SSP5-8.5 scenario be completed after downscaling the SSP3-7.0 and SSP1-2.6 scenarios, if computational resources allow for additional scenarios.

If the CORDEX modeling groups have sufficient resources, additional complementary simulations for other ensemble members and scenarios of the same GCM are also welcome.
It is up to the regional CORDEX communities to define a set of additional scenario simulations depending on resources and scientific questions.
It is strongly recommended that individual CORDEX RCM groups should coordinate their simulations with [CORDEX POCs](https://cordex.org/about/points-of-contact/) for respective domains in order to avoid uncoordinated efforts leading to sparse and unbalanced RCM-GCM matrices.

### GHG forcing

RCM groups should use the same scenario GHG forcing as in the driving CMIP6 models.
See for more details [Meinshausen et al. 2019](https://doi.org/10.5194/gmd-2019-222).

### Land use/Land cover

As the first step, it is recommended that the static land cover and land use maps that are a regional model’s default be used.
Recommendations for the implementation of a transient land use change (e.g., datasets, translation to RCMs, etc.) will be provided later.
When the recommendations become available, simulations with the static land cover and land use can be complemented by a number of new simulations with the transient land use change.

### Aerosol

A static aerosol dataset (e.g. a regional model’s default climatology) is considered as a minimum requirement.
It is recommended that for the scenario experiment RCM groups apply aerosol forcing which is either directly consistent with the driving CMIP6 GCMs or more broadly consistent with the CMIP6 aerosol forcing.
The first priority is given to aerosol optical properties (e.g., total aerosol optical depth or aerosol optical depth per species) provided by most CMIP6 GCMs.
General recommendations and more details are provided through [a dedicated document](https://cordex.org/wp-content/uploads/2021/02/aerosol4cordex.pdf) which will be regularly updated.
Comments and questions can be directly posted in [a living document](https://tinyurl.com/aerosol4cordex) or sent to the IPOC.

### Spectral nudging

It is up to RCM groups to decide on whether to apply large-scale spectral nudging for the CMIP6 scenario driven simulations or not.

## 7. RCM Documentation

Climate model documentation, providing all necessary details on model configurations, experiments, etc., is an integral part of climate modeling activities.
A coordinated effort to describe the models is still missing in CORDEX and currently there is no common system for collecting and providing RCM details, although work in this direction is ongoing.
Nonetheless, when possible, it is strongly recommended to create RCM documentation and errata, if necessary, that details all aspects of the experiments and make it publicly available by the regional communities.
Currently, a free format is assumed.

## 8. Selection of GCMs

There are a number of approaches but no commonly accepted methodology on how to select a subset of GCMs for downscaling.
Additionally, a subset of GCMs selected for one CORDEX domain is not necessarily an optimal choice for other domains.
It is up to the regional CORDEX communities to decide which CMIP6 models should be downscaled over a specific domain, considering for example: i) the ability of the CMIP6 models to simulate important aspects of regional and global climate, and ii) a range of plausible future climates simulated (e.g. regional temperature and precipitation responses) by the CMIP6 models with availability of forcing data.
It is also up to the regional CORDEX communities to decide on a minimum number of simulations and the design of RCM-GCM matrices for a specific domain, depending on resources available.

## 9. Output variables

The CORDEX Data Request (DR) details variables and frequencies to be saved and their priorities for delivery.
They can be found here: [https://github.com/WCRP-CORDEX/data-request-table](https://github.com/WCRP-CORDEX/data-request-table)

## 10. Archiving and publishing specifications

CORDEX output shall be published on the Earth System Grid Federation (ESGF) in order to be consistent with the CMIP6 archive and to make the output available to as many users as possible.
All CORDEX simulations have to be formatted according to the [CORDEX-CMIP6 archive specifications](https://doi.org/10.5281/zenodo.10961068) that provide technical aspects of CORDEX data format and guidance for publishing CORDEX data on ESGF.

!!! warning Note

    Once again, it is strongly recommended to avoid any uncoordinated  efforts and coordinate all activities with the POCs. If there are any questions and/or there is a need for guidance,  contact the POCs first. If this does not help, contact the IPOC.

## References

Gutowski Jr., W. J., Giorgi, F., Timbal, B., Frigon, A., Jacob, D., Kang, H.-S., Raghavan, K., Lee, B., Lennard, C., Nikulin, G., O'Rourke, E., Rixen, M., Solman, S., Stephenson, T., and Tangang, F.: WCRP COordinated Regional Downscaling EXperiment (CORDEX): a diagnostic MIP for CMIP6, Geosci. Model Dev., 9, 4087–4095, [https://doi.org/10.5194/gmd-9-4087-2016](https://doi.org/10.5194/gmd-9-4087-2016), 2016.

Meinshausen, M., Vogel, E., Nauels, A., Lorbacher, K., Meinshausen, N., Etheridge, D. M., Fraser, P. J., Montzka, S. A., Rayner, P. J., Trudinger, C. M., Krummel, P. B., Beyerle, U., Canadell, J. G., Daniel, J. S., Enting, I. G., Law, R. M., Lunder, C. R., O'Doherty, S., Prinn, R. G., Reimann, S., Rubino, M., Velders, G. J. M., Vollmer, M. K., Wang, R. H. J., and Weiss, R.: Historical greenhouse gas concentrations for climate modelling (CMIP6), Geosci. Model Dev., 10, 2057–2116, [https://doi.org/10.5194/gmd-10-2057-2017](https://doi.org/10.5194/gmd-10-2057-2017), 2017.

Meinshausen, M., Nicholls, Z., Lewis, J., Gidden, M. J., Vogel, E., Freund, M., Beyerle, U., Gessner, C., Nauels, A., Bauer, N., Canadell, J. G., Daniel, J. S., John, A., Krummel, P., Luderer, G., Meinshausen, N., Montzka, S. A., Rayner, P., Reimann, S., Smith, S. J., van den Berg, M., Velders, G. J. M., Vollmer, M., and Wang, H. J.: The SSP greenhouse gas concentrations and their extensions to 2500, Geosci. Model Dev. Discuss., [https://doi.org/10.5194/gmd-2019-222](https://doi.org/10.5194/gmd-2019-222), in review, 2019.

## Document history

### 2025-04-28

 * Add missing links to the archive specifications, data request and LBC availability table.
 * Add DOI and link to potential newer versions.
 * Fix several broken links.
 * Remove ES-DOC mention (not available anymore).
 * Use new logos and WCRP document template.

### 2021-05-18

 * Initial version

[^1]: [https://github.com/WCRP-CORDEX/domain-tables](https://github.com/WCRP-CORDEX/domain-tables)

[^2]: Not all CMIP6 GCMs provide enough data to drive RCMs. This list can be checked: [https://wcrp-cordex.github.io/cmip6-for-cordex/CMIP6_for_CORDEX_availability_RCM.html](https://wcrp-cordex.github.io/cmip6-for-cordex/CMIP6_for_CORDEX_availability_RCM.html)