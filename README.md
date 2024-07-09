# cleandirty_subs
This repository contains the replication code and data for Papaeorgiou, Saam and Schulte (2017). 

Reference: Papageorgiou, C., Saam, M. & Schulte, P. (2017). Substitution between Clean and Dirty Energy Inputs: A Macroeconomic Perspective. The Review of Economics and Statistics, 99 (2), 281–290. doi: https://doi.org/10.1162/REST_a_00592

The original publication of this code and data is: 
Papageorgiou, C., Saam, M. & Schulte, P. (2015). Replication data for: "Substitution between Clean and Dirty Energy Inputs - A Macroeconomic Perspective, https://doi.org/10.7910/DVN/67QCH2, Harvard Dataverse, V1, UNF:6:Xp3UuIfaJHq7CP13NoaD5w== [fileUNF] 


This readme-file describes how to replicate the results of the paper "Substitution between Clean and Dirty Energy Inputs - A Macroeconomic Perspective". To reproduce the results, the following source and data files have to be saved together in one folder. The generate_data.do uses the raw data files to generate the final data sets. The estimation.do produces all results provided in the paper. In order to run the two do-files in both it might be necessary to adjust the command (cd) which sets the working directory: the working directory has to be the folder in which all the replication files are saved.


[A] List of files 

1) Source code:
 - generate_data.do 			// do-file which uses the raw data file to generate the final data sets
 - estimation.do			// do-file which generates all results provided in the paper as well as some results from the online appendix

2) Raw data:				
 - flatfile_EM_may12.txt		// WIOD emission relevant energy use data (May 12 release)
 - IEA_elec_prices_NCV.xml		// IEA energy prices for electricity producers
 - IEA_ind_prices_NCV.xml		// IEA energy prices for industry
 - *_SUT_*.xls				// WIOD supply and use tables  (Jan/Feb 12 release)
 - IEA_elec_fuel.xls			// IEA data on fuel use in electricity generation
 - IEA_elec_cap.xls			// IEA data on electricity generation capacities by technology
 - IEA_elec_gen.xls			// IEA data on electricity generation by technology
 - flatfile_SEA.xls			// WIOD SEA data
 - PPP_*.xls				// GGDC PPP data

3) Final data sets:
 - electricity_sector.dta		// Electricity sector final data set
 - nonenergy_industries.dta		// Non-energy industries final data set

4) Results:
 - estimation_results.log		// log-file containing all estimation results
 

[B] Data dictionary

- electricity_sector.dta:

 country	26 countries	
 industry	1 industry (NACE 1.1)	
 year		1995 - 2009	
 EG_total	Net electricity production (GWh)  total plants  total	
 EC_total	Net electrical capacity  total plants  total	 
 EC_c		Net installed clean generation capacity (MW)	
 EC_d		Net installed dirty generation capacity (MW)	
 FU_c		Fuel input in clean electricity generating technologies (in TJ)	
 FU_d		Fuel input in dirty electricity generating technologies (in TJ)	
 FU_total	Fuel input in electricity generating technologies (in TJ)
 EC_c_alt	Alternative Capital Proxy: Capital stock associated with clean technologies (EIA based)
 EC_d_alt	Alternative Capital Proxy: Capital stock associated with dirty technologies (EIA based)

 
- nonenergy_industries.dta:

 country	19 countries			
 industry	28 industries (NACE 1.1)			
 sector		6 sectors			
 year		1995 - 2007			
 go		GO  Gross output at real 1997 US dollar (PPP)		
 xl		H_EMP  Total hours worked by persons engaged			
 xii		II  Intermediate inputs at real 1997 US dollar (PPP)			
 xk		K_GFCF  Real fixed capital stock, at real 1997 US dollar (PPP)			
 va		VA  Gross value added at real 1997 US dollar (PPP)			
 xe		Emission Relevant Energy Use (TJ) total			
 xiie		IIE  Intermediate energy inputs at real 1997 US dollar (PPP)			
 xiis		IIS  Intermediate service inputs at real 1997 US dollar (PPP)			
 xiim		IIM  Intermediate materials inputs at real 1997 US dollar (PPP)			
 xc		Emission relevant energy use of clean sources (TJ)			
 xd		Emission relevant energy use of dirty sources (TJ)			
 pk		Price of capital			
 pl		Price of hours worked			
 pc		Price of energy use of clean sources			
 pd		Price of energy use of dirty sources			
 sk		Cost share of capital			
 sl		Cost share of hours worked			
 sc		Cost share of energy use of clean sources			
 sd		Cost share of energy use of dirty sources
 xiims          IIS + IIM | Intermediate service and material inputs at real 1997 US dollar (PPP)
 vaxiie		VA + IIE | Gross value added plus intermediate energy inputs at real 1997 US dollar (PPP)			



[C] Software version used
 Stata/MP 12.1
 Windows 7 64bit
 or 
 Stata/MP 12.1
 Scientific Linux 6.4


[D] Contact data
 Chris Papageorgiou
 cpapageorgiou@imf.org


 Marianne Saam
 m.saam@zbw.eu

 Patrick Schulte
