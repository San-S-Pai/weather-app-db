FROM mysql:8.4.0-oracle

RUN echo  -e "[mysqld] \n"\ 
    "sql_mode = NO_ENGINE_SUBSTITUTION \n"\
    "gtid_mode = OFF_PERMISSIVE \n"\
    "performance_schema = 0 \n"\
    "persisted_globals_load = 0 \n"\
    "local_infile = 1 \n"\
    "binlog_format = MIXED \n"\
    "log_statements_unsafe_for_binlog = 0 \n"\
    "block_encryption_mode = aes-256-cbc \n"\
    "log_bin_trust_function_creators = 1" >> /etc/mysql/conf.d/my-custom.cnf

RUN microdnf install -y tar git