Classical PSHA using Area Source
================================

=============================================== ========================
tstation.gem.lan:/mnt/ssd/oqdata/calc_1863.hdf5 Fri Jul  7 07:33:36 2017
checksum32                                      1,205,782,117           
engine_version                                  2.6.0-git50066b9        
=============================================== ========================

num_sites = 6, num_imts = 3

Parameters
----------
=============================== ==================
calculation_mode                'classical'       
number_of_logic_tree_samples    0                 
maximum_distance                {'default': 200.0}
investigation_time              50.0              
ses_per_logic_tree_path         1                 
truncation_level                3.0               
rupture_mesh_spacing            2.0               
complex_fault_mesh_spacing      2.0               
width_of_mfd_bin                0.2               
area_source_discretization      5.0               
ground_motion_correlation_model None              
random_seed                     23                
master_seed                     0                 
=============================== ==================

Input files
-----------
======================= ============================================================
Name                    File                                                        
======================= ============================================================
gsim_logic_tree         `gmpe_logic_tree.xml <gmpe_logic_tree.xml>`_                
job_ini                 `job.ini <job.ini>`_                                        
source                  `source_model.xml <source_model.xml>`_                      
source_model_logic_tree `source_model_logic_tree.xml <source_model_logic_tree.xml>`_
======================= ============================================================

Composite source model
----------------------
========= ====== ====================================== =============== ================
smlt_path weight source_model_file                      gsim_logic_tree num_realizations
========= ====== ====================================== =============== ================
b1        1.000  `source_model.xml <source_model.xml>`_ simple(2)       2/2             
========= ====== ====================================== =============== ================

Required parameters per tectonic region type
--------------------------------------------
====== ===================================== =========== ======================= =================
grp_id gsims                                 distances   siteparams              ruptparams       
====== ===================================== =========== ======================= =================
0      BooreAtkinson2008() ChiouYoungs2008() rjb rrup rx vs30 vs30measured z1pt0 dip mag rake ztor
====== ===================================== =========== ======================= =================

Realizations per (TRT, GSIM)
----------------------------

::

  <RlzsAssoc(size=2, rlzs=2)
  0,BooreAtkinson2008(): ['<0,b1~b1,w=0.6>']
  0,ChiouYoungs2008(): ['<1,b1~b2,w=0.4>']>

Number of ruptures per tectonic region type
-------------------------------------------
================ ====== ==================== =========== ============ ============
source_model     grp_id trt                  num_sources eff_ruptures tot_ruptures
================ ====== ==================== =========== ============ ============
source_model.xml 0      Active Shallow Crust 1           9840         1,640       
================ ====== ==================== =========== ============ ============

Informational data
------------------
============================== ==================================================================================
count_eff_ruptures.received    tot 3.47 KB, max_per_task 592 B                                                   
count_eff_ruptures.sent        sources 11.17 KB, param 6.97 KB, srcfilter 4.01 KB, monitor 1.89 KB, gsims 1.05 KB
hazard.input_weight            164.0                                                                             
hazard.n_imts                  3                                                                                 
hazard.n_levels                57                                                                                
hazard.n_realizations          2                                                                                 
hazard.n_sites                 6                                                                                 
hazard.n_sources               1                                                                                 
hazard.output_weight           684.0                                                                             
hostname                       tstation.gem.lan                                                                  
require_epsilons               False                                                                             
============================== ==================================================================================

Slowest sources
---------------
====== ========= ============ ============ ========= ========= =========
grp_id source_id source_class num_ruptures calc_time num_sites num_split
====== ========= ============ ============ ========= ========= =========
0      1         AreaSource   1,640        0.007     1         6        
====== ========= ============ ============ ========= ========= =========

Computation times by source typology
------------------------------------
============ ========= ======
source_class calc_time counts
============ ========= ======
AreaSource   0.007     1     
============ ========= ======

Information about the tasks
---------------------------
================== ===== ========= ===== ===== =========
operation-duration mean  stddev    min   max   num_tasks
count_eff_ruptures 0.002 3.157E-04 0.002 0.002 6        
================== ===== ========= ===== ===== =========

Slowest operations
------------------
============================== ========= ========= ======
operation                      time_sec  memory_mb counts
============================== ========= ========= ======
reading composite source model 0.037     0.0       1     
managing sources               0.016     0.0       1     
total count_eff_ruptures       0.012     0.0       6     
prefiltering source model      0.008     0.0       7     
store source_info              0.003     0.0       1     
reading site collection        0.002     0.0       1     
aggregate curves               9.084E-05 0.0       6     
saving probability maps        2.503E-05 0.0       1     
============================== ========= ========= ======