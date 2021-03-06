North Africa PSHA
=================

============== ===================
checksum32     3,672,594,697      
date           2019-05-03T06:44:12
engine_version 3.5.0-git7a6d15e809
============== ===================

num_sites = 2, num_levels = 133, num_rlzs = 8

Parameters
----------
=============================== ==================
calculation_mode                'preclassical'    
number_of_logic_tree_samples    0                 
maximum_distance                {'default': 200.0}
investigation_time              50.0              
ses_per_logic_tree_path         1                 
truncation_level                3.0               
rupture_mesh_spacing            2.0               
complex_fault_mesh_spacing      2.0               
width_of_mfd_bin                0.1               
area_source_discretization      10.0              
ground_motion_correlation_model None              
minimum_intensity               {}                
random_seed                     19                
master_seed                     0                 
ses_seed                        42                
=============================== ==================

Input files
-----------
======================= ============================================================
Name                    File                                                        
======================= ============================================================
gsim_logic_tree         `gmpe_logic_tree.xml <gmpe_logic_tree.xml>`_                
job_ini                 `job.ini <job.ini>`_                                        
sites                   `sites.csv <sites.csv>`_                                    
source_model_logic_tree `source_model_logic_tree.xml <source_model_logic_tree.xml>`_
======================= ============================================================

Composite source model
----------------------
============================= ======= =============== ================
smlt_path                     weight  gsim_logic_tree num_realizations
============================= ======= =============== ================
smoothed_model_m_m0.2_b_e0.0  0.50000 simple(0,4,0)   4               
smoothed_model_m_m0.2_b_m0.05 0.50000 simple(0,4,0)   4               
============================= ======= =============== ================

Required parameters per tectonic region type
--------------------------------------------
====== ============================================================================================== =========== ======================= =================
grp_id gsims                                                                                          distances   siteparams              ruptparams       
====== ============================================================================================== =========== ======================= =================
0      '[AkkarEtAlRjb2014]' '[AtkinsonBoore2006Modified2011]' '[ChiouYoungs2014]' '[PezeshkEtAl2011]' rjb rrup rx vs30 vs30measured z1pt0 dip mag rake ztor
1      '[AkkarEtAlRjb2014]' '[AtkinsonBoore2006Modified2011]' '[ChiouYoungs2014]' '[PezeshkEtAl2011]' rjb rrup rx vs30 vs30measured z1pt0 dip mag rake ztor
====== ============================================================================================== =========== ======================= =================

Realizations per (GRP, GSIM)
----------------------------

::

  <RlzsAssoc(size=8, rlzs=8)
  0,'[AkkarEtAlRjb2014]': [1]
  0,'[AtkinsonBoore2006Modified2011]': [2]
  0,'[ChiouYoungs2014]': [0]
  0,'[PezeshkEtAl2011]': [3]
  1,'[AkkarEtAlRjb2014]': [5]
  1,'[AtkinsonBoore2006Modified2011]': [6]
  1,'[ChiouYoungs2014]': [4]
  1,'[PezeshkEtAl2011]': [7]>

Number of ruptures per tectonic region type
-------------------------------------------
=============== ====== =============== ============ ============
source_model    grp_id trt             eff_ruptures tot_ruptures
=============== ====== =============== ============ ============
GridSources.xml 0      Tectonic_type_b 260          260         
GridSources.xml 1      Tectonic_type_b 260          260         
=============== ====== =============== ============ ============

============= ===
#TRT models   2  
#eff_ruptures 520
#tot_ruptures 520
#tot_weight   52 
============= ===

Slowest sources
---------------
====== ========= ==== ===== ===== ============ ========= ========= ======
grp_id source_id code gidx1 gidx2 num_ruptures calc_time num_sites weight
====== ========= ==== ===== ===== ============ ========= ========= ======
0      21        M    0     2     260          0.00149   1.00000   26    
1      21        M    2     4     260          6.995E-04 1.00000   26    
====== ========= ==== ===== ===== ============ ========= ========= ======

Computation times by source typology
------------------------------------
==== ========= ======
code calc_time counts
==== ========= ======
M    0.00219   2     
==== ========= ======

Duplicated sources
------------------
['21']
Found 1 source(s) with the same ID and 1 true duplicate(s)

Information about the tasks
---------------------------
================== ======= ========= ======= ======= =======
operation-duration mean    stddev    min     max     outputs
read_source_models 0.00204 5.808E-04 0.00163 0.00245 2      
preclassical       0.00415 0.00188   0.00282 0.00547 2      
================== ======= ========= ======= ======= =======

Data transfer
-------------
================== ========================================================= ========
task               sent                                                      received
read_source_models converter=626 B fnames=212 B                              3.9 KB  
preclassical       params=3.82 KB srcs=3.08 KB gsims=1.23 KB srcfilter=436 B 672 B   
================== ========================================================= ========

Slowest operations
------------------
======================== ========= ========= ======
operation                time_sec  memory_mb counts
======================== ========= ========= ======
total preclassical       0.00829   0.0       2     
total read_source_models 0.00408   0.0       2     
managing sources         0.00295   0.0       1     
store source_info        0.00199   0.0       1     
aggregate curves         2.403E-04 0.0       2     
======================== ========= ========= ======