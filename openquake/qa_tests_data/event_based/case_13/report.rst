Event Based QA Test, Case 13
============================

=============================================== ========================
tstation.gem.lan:/mnt/ssd/oqdata/calc_1836.hdf5 Fri Jul  7 07:33:02 2017
checksum32                                      3,958,324,456           
engine_version                                  2.6.0-git50066b9        
=============================================== ========================

num_sites = 1, num_imts = 1

Parameters
----------
=============================== ==================
calculation_mode                'event_based'     
number_of_logic_tree_samples    0                 
maximum_distance                {'default': 200.0}
investigation_time              1.0               
ses_per_logic_tree_path         5000              
truncation_level                2.0               
rupture_mesh_spacing            1.0               
complex_fault_mesh_spacing      1.0               
width_of_mfd_bin                1.0               
area_source_discretization      10.0              
ground_motion_correlation_model None              
random_seed                     42                
master_seed                     0                 
=============================== ==================

Input files
-----------
======================= ============================================================
Name                    File                                                        
======================= ============================================================
gsim_logic_tree         `gsim_logic_tree.xml <gsim_logic_tree.xml>`_                
job_ini                 `job.ini <job.ini>`_                                        
source                  `source_model.xml <source_model.xml>`_                      
source_model_logic_tree `source_model_logic_tree.xml <source_model_logic_tree.xml>`_
======================= ============================================================

Composite source model
----------------------
========= ====== ====================================== =============== ================
smlt_path weight source_model_file                      gsim_logic_tree num_realizations
========= ====== ====================================== =============== ================
b1        1.000  `source_model.xml <source_model.xml>`_ trivial(1)      1/1             
========= ====== ====================================== =============== ================

Required parameters per tectonic region type
--------------------------------------------
====== =================== ========= ========== ==========
grp_id gsims               distances siteparams ruptparams
====== =================== ========= ========== ==========
0      BooreAtkinson2008() rjb       vs30       mag rake  
====== =================== ========= ========== ==========

Realizations per (TRT, GSIM)
----------------------------

::

  <RlzsAssoc(size=1, rlzs=1)
  0,BooreAtkinson2008(): ['<0,b1~b1,w=1.0>']>

Number of ruptures per tectonic region type
-------------------------------------------
================ ====== ==================== =========== ============ ============
source_model     grp_id trt                  num_sources eff_ruptures tot_ruptures
================ ====== ==================== =========== ============ ============
source_model.xml 0      Active Shallow Crust 1           1            1           
================ ====== ==================== =========== ============ ============

Informational data
------------------
============================ ==========================================================================
compute_ruptures.received    max_per_task 81.01 KB, tot 81.01 KB                                       
compute_ruptures.sent        sources 1.29 KB, src_filter 684 B, param 606 B, monitor 320 B, gsims 102 B
hazard.input_weight          0.1                                                                       
hazard.n_imts                1                                                                         
hazard.n_levels              3                                                                         
hazard.n_realizations        1                                                                         
hazard.n_sites               1                                                                         
hazard.n_sources             1                                                                         
hazard.output_weight         50.0                                                                      
hostname                     tstation.gem.lan                                                          
require_epsilons             False                                                                     
============================ ==========================================================================

Slowest sources
---------------
====== ========= ============ ============ ========= ========= =========
grp_id source_id source_class num_ruptures calc_time num_sites num_split
====== ========= ============ ============ ========= ========= =========
0      1         PointSource  1            0.0       1         0        
====== ========= ============ ============ ========= ========= =========

Computation times by source typology
------------------------------------
============ ========= ======
source_class calc_time counts
============ ========= ======
PointSource  0.0       1     
============ ========= ======

Information about the tasks
---------------------------
================== ===== ====== ===== ===== =========
operation-duration mean  stddev min   max   num_tasks
compute_ruptures   0.038 NaN    0.038 0.038 1        
================== ===== ====== ===== ===== =========

Slowest operations
------------------
============================== ========= ========= ======
operation                      time_sec  memory_mb counts
============================== ========= ========= ======
total compute_ruptures         0.038     0.0       1     
setting event years            0.031     0.0       1     
saving ruptures                0.025     0.0       1     
store source_info              0.006     0.0       1     
reading composite source model 0.002     0.0       1     
managing sources               0.001     0.0       1     
prefiltering source model      5.870E-04 0.0       1     
filtering ruptures             5.076E-04 0.0       1     
reading site collection        4.435E-05 0.0       1     
============================== ========= ========= ======