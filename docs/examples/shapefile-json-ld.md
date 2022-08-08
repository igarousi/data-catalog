# Simple Shapefile Example

The document contains an example implementation of SchemaOrg for a basic
Shapefile as outlined [here](shapefile.md). This implementation closely follows
the recommendations of the [ESIP community](https://github.com/ESIPFed/science-on-schema.org/blob/226-esip-summer-mtg-2022-tutorial/tutorials/esip-summer-mtg-2022/README.md).

The `json+ld` below is derived from the content located
[here](https://hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51).

``` json
{
  "@context": "https://schema.org/",
  "@type": "Dataset",
  "name": "IGUIDE Shapefile Testing Resource",
  "description": "This resource contains medium-resolution (1:100k) National Hydrography Dataset (NHDPlus) [1] map data for a region of 39 Hydrologic Unit Code (HUC) 6-digit (HUC6) basins around the Hurricane Harvey impact zone across Texas, Louisiana, Mississippi and Arkansas. This includes 5978 subwatersheds, 190,192 catchments, and 192,267 flowlines. USGS active stream gages (924) were downloaded from the USGS National Water Information System (NWIS) [2] and augmented with each gage's HUC2, HUC4, HUC6, HUC8, HUC10 & HUC12 basin identifiers, and COMID of the NHD stream reach for the containing catchment. This allows the user to easily aggregate gages by various watershed boundaries. NOAA Advanced Hydrologic Prediction System (AHPS) [3] has 362 river forecast points in the Harvey study area. Many of these are co-located with USGS NWIS gages to leverage authoritative observation data. A shapefile of Texas dams (7290) was directly received from the Texas Commission for Environmental Quality (TCEQ) [4]. They suggest if you have any questions about data, to make an Open Records Request [5].",
  "url":
  "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/",
  "dateCreated": "2022-08-02",
  "dateModified": "2022-08-02",
  "contentReferenceTime": "2022-08-02T16:38:00-05:00Z",
  "creativeWorkStatus": "Public",
  "keywords": [
    "NHD", 
    "hydrolog", 
    "NHDPlus", 
    "gages", 
    "NWIS", 
    "reaches", 
    "catchments", 
    "dams", 
    "AHPS", 
    "TCEQ", 
    "USGS", 
    "Harvey2017"
  ],
  "creator": {
    "@list":[
      {
        "@type": "Organization",
        "name": "U.S. Geological Survey (USGS)"
      },
      {
        "@type": "Organization",
        "name": "NOAA National Weather Service"
      },
      {
        "@type": "Organization",
        "name": "Texas Commission for Environmental Quality (TCEQ)"
      },
      {
        "@type": "Person",
        "name": "David Arctur",
	"email": "david.arctur@utexas.edu",
	"identifier": {
	  "@id": "https://orcid.org/0000-0002-4708-6302",
	  "@type": "PropertyValue",
	  "propertyID": "https://registry.identifiers.org/registry/orcid",
	  "url": "https://orcid.org/0000-0002-4708-6302",
	  "value": "0000-0002-4708-6302"
	}
      }
    ]
  },
  "spatialCoverage": {
    "@type": "Place",
    "geo": {
      "@type": "GeoShape",
      "polygon": "-101.05799349299997,34.99981308000001 -88.02901011799993,34.99981308000001 -88.02901011799993,25.837074428000108 -101.05799349299997,25.837074428000108 -101.05799349299997,34.99981308000001"
    },
    "additionalProperty": {
      "@type": "PropertyValue",
      "propertyID":"http://dbpedia.org/resource/Spatial_reference_system",
      "value": "http://www.w3.org/2003/01/geo/wgs84_pos#lat_long"
    }
  },
  "funding": [
    {
      "@type": "MonetaryGrant",
      "name": "RAPID: Archiving and Enabling Community Access to Data from Recent US Hurricanes",
      "url": "https://www.nsf.gov/awardsearch/showAward?AWD_ID=1761673",
      "funder": {
        "@type": "Organization",
        "name": "National Science Foundation"
      }
    }
  ],
  "subjectOf": {
    "@type": "DataDownload",
    "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/resourcemetadata.xml",
    "encodingFormat": "application/xml",
    "contentSize": "7.7 MB",
    "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "b2c9a5c14fd55003e404135ed2757a05",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
  },
  "distribution": [
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.shp.xml",
      "encodingFormat": "application/fgdc+xml",
      "contentSize": "88.0 KB",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "c66f87f4b3653c7e620e45bb232a608f",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.shx",
      "encodingFormat": "x-gis/x-shapefile",
      "contentSize": "412.0 B",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "38e2378570d2ff63df78d8cbbf86d14c",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.shp",
      "encodingFormat": "x-gis/x-shapefile",
      "contentSize": "7.6 MB",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "516aa62d19ec58652e528e06b75c43c9",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.sbx",
      "encodingFormat": "x-gis/x-shapefile",
      "contentSize": "164 B",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "821c450cbc3c6704555a7c55ff98ee16",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.sbn",
      "encodingFormat": "x-gis/x-shapefile",
      "contentSize": "532 B",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "d9e624f105e43fc0dde19c987eb2daa5",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.prj",
      "encodingFormat": "application/text",
      "contentSize": "167.0 B",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "8e24fe15b2c8c640c459006722fa1e7f",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.dbf",
      "encodingFormat": "application/octet-stream",
      "contentSize": "1.8 KB",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "4aad28f03ec1bc03e15f7a73d122cd2a",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    },
    {
      "@type": "DataDownload",
      "contentUrl": "https://www.hydroshare.org/resource/9d413b9d57824a79b8239a5f7c4fdf51/data/contents/HUC6_Harvey_TxLaMsAr.cpg",
      "encodingFormat": "x-gis/x-shapefile",
      "contentSize": "5.0 B",
      "spdx:checksum": {
        "@type": "spdx:Checksum",
        "spdx:checksumValue": "ae3b3df9970b49b6523e608759bc957d",
        "spdx:checksumAlgorithm": {
          "@id": "spdx:checksumAlgorithm_md5"
        }
      }
    }
  ],
  "variableMeasured": [
    {
      "@type": "PropertyValue",
      "propertyID": "HUC_6",
      "value": "String"
    },
    {
      "@type": "PropertyValue",
      "propertyID": "Shape_Leng",
      "value": "Real"
    },
    {
      "@type": "PropertyValue",
      "propertyID": "Shape_Area",
      "value": "Real"
    }
  ]
}
```