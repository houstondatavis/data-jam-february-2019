# data-jam-february-2019
Cleveland Museum of Art API


## Important Links to original dataset information

### The datasets github page https://github.com/ClevelandMuseumArt/openaccess
The main pieces in this github repository are a README markdown file with information, a CSV, and a JSON. The CSV and the JSON are very very large, 59MB and 172MB respectively. You probably don't want to work with these files directly as they would take up a lot of space and be slow to work with.

The API equivelant of the JSON Provided at the link above is: `https://openaccess-api.clevelandart.org/api/artworks/`

### The datasets webpage http://openaccess-api.clevelandart.org/
This webpage has general information as well as fields, query parameters, and examples requests to the API. 

## A smaller data subset to work with in CSV format

## Important things you might want to know
1. About half the artworks have a creative commons license and about have don't. You may want to limit your calls to only artworks that have a creative commons licesnse so that way you don't have to worry about a license that precludes... things? An example of quering all the artworks that have the creative commons zero license is `https://openaccess-api.clevelandart.org/api/artworks/?cc0=0`. That will return a json of ~27,000 artworks.

## Possible ideas


## Twitter handles & hashtags to share your visualizations with
