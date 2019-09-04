# smart-ad

Ad service to get localized ads for selected client and project.

## Authentication & localized response
Url for localized request: https://ad.smart-byte.com/location

When establishing connection client must send credentials

Example for request http reuqest header:
```
Content-Type: application/json
{
  	"clientId": "2d75511d-73c2-4eae-9d39-1738b5f2abe2",
  	"password" : "***********",
  	"projectId": "4c0bf3d5-a218-4aaa-8c03-eb210ee5f848",
  	"device" : {
		"identifer" : "{UUID , created on first app start!!!}",
  		"platform" : "{please add correct device platform from device data: e.g iOS}",
  		"os" : "{please add correct os version from device os data: e.g for iOS  12.x/ Android xy}",
  		"model" : "{please add correct model code from device data: e.g 4,6}",
  		"vendor" : "{please add correct device vendor from device data: e.g Apple/Samsung }"
  	},
  	"location" : {
  		"latitude" : 48.135124,
  		"longitude" : 11.581981
  	},
  	"timestamp" : 1523875370
  }

```

Response will be a Html Content page.

If request url contains "json" at the end like:

Url for localized request: https://ad.smart-byte.com/location/json

response:
```
{
	"id": "6707ed46-03ff-4882-b91f-51cc5bad2a05",
	"type": "intersticial",
	"authorized": true,
	"url": "https:\/\/ad.smart-byte.com\/content\/html\/6707ed46-03ff-4882-b91f-51cc5bad2a05",
	"duration": 1800
}
```
