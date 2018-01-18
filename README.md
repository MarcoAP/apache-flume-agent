# apache-flume-agent
# Dois agents Flume enviando stream de dados um para o outro. [Spooldir - Avro]

# Objetivo:

## Agent-From lê um diretório Spooldir e envia para localhost (você pode alterar o IP e Porta neste caso) Avro:

### [execução] ###

$ sudo flume-ng agent -n agent-from -c /etc/flume-ng/conf/* -f /home/analytics/flume-agent/agent_s3_from.properties

# ====================================================================

## Agent-TO recebe os dados do Sink do Agent-From e grava em um diretório (você pode alterar este path no seu hdfs) no hdfs:

### [execução] ###

$ sudo flume-ng agent -n agent-to -c /etc/flume-ng/conf/* -f /home/analytics/flume-agent/agent_s3_to.properties
