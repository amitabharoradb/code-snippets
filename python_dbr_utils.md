## How to use Boolean notebook widgets
```python
reset_all_data = dbutils.widgets.get("reset_all_data") == "true"
```

## Define scmema variables
```python
schema = dbName = db = "dbdemos_feature_store"
```

## Check if a volume exists
```python
try:
  dbutils.fs.ls(volume_folder+"/transactions")
  dbutils.fs.ls(volume_folder+"/customers")
except:  
  print(f"folder doesn't exists, generating the data under {volume_folder}...")
```

## How to read data from Marketplace
[Example of "Load Retail Catalog from Marketplace"](https://e2-demo-field-eng.cloud.databricks.com/editor/notebooks/567797471593961?o=1444828305810485#command/7578492502727050)