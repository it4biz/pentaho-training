## Shell Script (Linux and Mac OS)
```
echo "Start PDI Job"
cd /Applications/Pentaho/5.4.0/data-integration
./kitchen.sh -file:/Users/caiomsouza/Dropbox/BI-Suite-Set2015/ETLs/3.Cargas/j_carga_dm_vendas.kjb -level:Basic
```

## Bat Script (Windows) 
``` 
echo "Executando job - Kettle Cookbook"
cd "C:\Users\caiomsouza\Desktop\Pentaho\pdi-ce-5.4.0.1-130\data-integration"
.\Kitchen.bat /file:C:\Users\caiomsouza\Desktop\Pentaho\ETLs\j_carga_dm_vendas.kjb /level:Basic > C:\Users\caiomsouza\Desktop\Pentaho\ETLs\logs\job.log
```

## Bat Script (Windows) for Kettle Cookbook
```
echo "Executando job - Kettle Cookbook"
cd "C:\Users\caiomsouza\Desktop\Pentaho\pdi-ce-5.4.0.1-130\data-integration"
.\Kitchen.bat /file:C:\Users\caiomsouza\Desktop\Pentaho\ETLs\it4biz-kettle-cookbook\pdi\document-folder.kjb "/param:INPUT_DIR=C:\Users\caiomsouza\Desktop\Pentaho\ETLs" "/param:OUTPUT_DIR=C:\Users\caiomsouza\Desktop\Pentaho\ETLs\docs\doc-it4biz-kettle-cookbook" "/param:SAXON=.\lib\saxon-9.1.0.8.jar" /level:Basic > C:\Users\caiomsouza\Desktop\Pentaho\ETLs\logs\job_kettle-cookbook.log
```
