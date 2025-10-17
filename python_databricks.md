## Check if a volume exists
```python
try:
  dbutils.fs.ls(volume_folder+"/transactions")
  dbutils.fs.ls(volume_folder+"/customers")
except:  
  print(f"folder doesn't exists, generating the data under {volume_folder}...")

```

## Define an empty config object
```python
if 'config' not in locals():
  config = {}
```