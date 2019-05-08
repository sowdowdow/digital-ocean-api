# digital-ocean-api 🌊
__Work in progress /!\🚧🚧🚧__

A simple python wrapper for the Digital Ocean's API

## Example usage

```py
api = DigitalOceanAPIv2(bearer='<your_api_token>')
print(api.rate_limit())
# OUTPUT
# {'Limit': '5000', 'Remaining': '4951', 'Reset': '1557328997'}
```
### Getting the list of regions available

```py
print(api.list_regions())
# OUTPUT
{
    'links': {},
    'meta': {'total': 9},
    'regions': [{'available': True,
                 'features': ['private_networking',
                              '...',
                              'image_transfer'],
                 'name': 'New York 1',
                 'sizes': ['32gb',
                           '512mb',
                           's-1vcpu-3gb',
                           'c-2',
                           '...',
                           'gd-2vcpu-8gb'],
                 'slug': 'nyc1'},
                ]}
```
