Group Servers Summary
=========================

Group Servers Configuration
------------------------------------

There are two servers available for use and the configuration are shown as below:

.. list-table:: Group Servers Configuration
   :widths: 10 45 45
   :header-rows: 1

   * - 
     - Server 1
     - Server 2
   * - CPU
     - 4x Intel Xeon Gold 6134
     - 2x lntel Xeon Gold 6230
   * - GPU
     - None
     - 8x GeForce RTX 2080 Ti 
   * - RAM
     - 24x 64GB LRDIMM
     - Row 2, column 3
   * - Storage
     - 12x 1.92TB SSD (Shareable)
     - 1x 3840GB + 1x 1.92TB SSD (Shareable)
   * - Back-up
     - None
     - None

General Rule
----------------------
* Never use ``sudo`` or ``su`` unless you approval from both Professor and RHCSA.
* If any of server is in high utilization and you need computation resources, contact Dr. Zoe Li or Tianshuo Li for coordination.
* Please use server 2 for computation tasks required GPU (e.g. modeling training, parallel processing), and server 1 for other tasks (e.g. downloading data, file processing). The disk on both server are shareable so please do not worry about data transferring stuff.