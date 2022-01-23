# gofile-client
A wrapper around the [gofile.io API](https://gofile.io/api).

## Installation
### via [`pip`](https://pip.pypa.io/en/stable/installation/)
```
pip install --user gofile-client
```

## Usage
```python
from gofile.client import Gofile

client = Gofile(token='<your-token>')

# Upload a file
response = client.upload_file('path/to/file')
print(response)

# Get the link to a file
folder_contents = client.get_content('<file-id>')
for _, item in folder_contents:
    print(item['link'])
```
