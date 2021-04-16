# base


Python base image including :

- Oracle Instant Client
- SAP NFRFC SDK
- pymssql
- pymysql 
- pyrfc
- exchangelib
- xlrd
- pyhive
- cx_Oracle


How to Use

- docker run -i --name voila -d -t   -p 10000:80 -v /home/docker/voila/voila_notebooks:/opt/voila_notebooks muyouming/base /bin/bash -c "/opt/conda/bin/pip install -i http://pypi.douban.com/simple --trusted-host pypi.douban.com -r /opt/voila_notebooks/requirements.txt && cd /opt/voila_notebooks && /opt/conda/bin/voila --MappingKernelManager.cull_interval=60 --MappingKernelManager.cull_idle_timeout=120 --enable_nbextensions=True --template=flex  --ip=0.0.0.0  --port=80 --no-browser --Voila.base_url=/v1/"


How to delete
- docker rm --force  voila
