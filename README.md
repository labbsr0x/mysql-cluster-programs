![logo](https://www.mysql.com/common/logos/logo-mysql-170x115.png)
## What is the porpuse of this image?

If you run **MySQL Cluster** with Docker from the official image you will notice that the image was built using the **minimal** version of the MySQL Cluster Server. This means that the image doesn't have all the tooling you'll need to play around and manage MySQL Cluster. That makes sense since you want the most optimized version of the server in a production environment, but you still need a tooling belt to get your stuff done. 

## So what?

We built an MySQL Cluster image with all those toolings, i.e., the [NDB Cluster Programs](https://dev.mysql.com/doc/mysql-cluster-excerpt/5.7/en/mysql-cluster-programs.html). Those are specialized pieces of code provided by MySQL itself that are used to manage NDB Clusters, including Data and SQL Node processes (ndbd, ndbmtd, ndb_mgmd, and mysqld) and the management client (ndb_mgm). The list of programs included are:

* ndbd — The NDB Cluster Data Node Daemon
* ndbinfo_select_all — Select From ndbinfo Tables
* ndbmtd — The NDB Cluster Data Node Daemon (Multi-Threaded)
* ndb_mgmd — The NDB Cluster Management Server Daemon
* ndb_mgm — The NDB Cluster Management Client
* ndb_blob_tool — Check and Repair BLOB and TEXT columns of NDB Cluster Tables
* ndb_config — Extract NDB Cluster Configuration Information
* ndb_cpcd — Automate Testing for NDB Development
* ndb_delete_all — Delete All Rows from an NDB Table
* ndb_desc — Describe NDB Tables
* ndb_drop_index — Drop Index from an NDB Table
* ndb_drop_table — Drop an NDB Table
* ndb_error_reporter — NDB Error-Reporting Utility
* ndb_import — Import CSV Data Into NDB
* ndb_index_stat — NDB Index Statistics Utility
* ndb_move_data — NDB Data Copy Utility
* ndb_perror — Obtain NDB error message information
* ndb_print_backup_file — Print NDB Backup File Contents
* ndb_print_file — Print NDB Disk Data File Contents
* ndb_print_frag_file — Print NDB Fragment List File Contents
* ndb_print_schema_file — Print NDB Schema File Contents
* ndb_print_sys_file — Print NDB System File Contents
* ndb_redo_log_reader — Check and Print Content of Cluster Redo Log
* ndb_restore — Restore an NDB Cluster Backup     
* ndb_select_all — Print Rows from an NDB Table
* ndb_select_count — Print Row Counts for NDB Tables
* ndb_setup.py — Start browser-based Auto-Installer for NDB Cluster
* ndb_show_tables — Display List of NDB Tables
* ndb_size.pl — NDBCLUSTER Size Requirement Estimator
* ndb_top — View CPU usage information for NDB threads
* ndb_waiter — Wait for NDB Cluster to Reach a Given Status
* Options Common to NDB Cluster Programs — Options Common to NDB Cluster Programs