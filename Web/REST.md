# POST call
```python
# Set up credentials
export DATABRICKS_TOKEN=...

url = "https://{workspace_url}/serving-endpoints/user-preferences/invocations"

headers = {'Authorization': f'Bearer {DATABRICKS_TOKEN}', 'Content-Type': 'application/json'}

data = {
  "dataframe_records": [{"user_id": user_id}]
}
data_json = json.dumps(data, allow_nan=True)

response = requests.request(method='POST', headers=headers, url=url, data=data_json)
if response.status_code != 200:
  raise Exception(f'Request failed with status {response.status_code}, {response.text}')

print(response.json()['outputs'][0]['hotel_preference'])
```