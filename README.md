# data-jam-february-2019
Cleveland Museum of Art API


## Important Links to original dataset information

### The datasets github page https://github.com/ClevelandMuseumArt/openaccess
The main pieces in this github repository are a README markdown file with information, a CSV, and a JSON. The CSV and the JSON are very large, 59MB and 172MB respectively. You may not want to work with these files directly as they would take up a lot of space and be slow to work with.

The API equivelant of the JSON Provided at the link above is: `https://openaccess-api.clevelandart.org/api/artworks/`

### The datasets webpage http://openaccess-api.clevelandart.org/
This webpage has general information as well as fields, query parameters, and examples requests to the API. 

## A smaller data subset to work with in CSV format

## Important things you might want to know
1. About _half the artworks have a creative commons license_ and about have don't. You may want to limit your calls to only artworks that have a creative commons licesnse so that way you don't have to worry about a license that precludes... things? An example of quering all the artworks that have the creative commons zero license is `https://openaccess-api.clevelandart.org/api/artworks/?cc0=0`. That will return a json of ~27,000 artworks.
2. You can *combine two queries* using a & like so `https://openaccess-api.clevelandart.org/api/artworks/?cc0=1&department=Textiles&has_image=1` To get a list of queries see, the Parameters table at http://openaccess-api.clevelandart.org/
3. You can either do a *query for a json of artworks or request a json for a specific piece of art*. To do the later, you can use <b>either</b> Athena id or accession number. Both return the same result. For example, both `https://openaccess-api.clevelandart.org/api/artworks/130707?indent=1` and `https://openaccess-api.clevelandart.org/api/artworks/1953.424?indent=1` return the same json. One uses the Athena id and the other the accession number for the API call. The syntax is the same, just different numbers used.
4. Not all the artwork results you'll get back have an image but some do. You can use the `has_image` parameter to *limit your search to those that have an image*. This looks like `https://openaccess-api.clevelandart.org/api/artworks/?cc0=1&department=Textiles&has_image=1`. You won't get back the image yet, however. There are several image files in the returned json. Different ones lead to different sized images. The smallest is `"images":{"web":{"url":`<url you want is here>`}}` as seen below. An example image is https://openaccess-cdn.clevelandart.org/1953.129/1953.129_web.jpg . The individual artwork json that goes with that image is https://openaccess-api.clevelandart.org/api/artworks/1953.129?indent=1 .

MUCH MORE OF THIS TYPE OF INFORMATION CAN BE FOUND AT: http://openaccess-api.clevelandart.org/



## Example Google Colab Notebook that calls API and creates a CSV instead of JSON for additional use
- This is a quick way to get smaller CSVs to work with, so you don't have to work with the API directly if you don't want to.
- It is also a good demo for how to call the API in Python and get results back.
https://colab.research.google.com/drive/1nBpqLjbPuZxnaotZn9o50yxWUE3nd0f4

## Random possible ideas of various degrees of liklihood of getting done in <4 hours
- Create user interface on <a href="https://beta.observablehq.com/">ObservableHQ</a> that changes parameters quered and generates gallery on ObservableHQ, similar to this gallery generated from the NASA Apod API. https://beta.observablehq.com/@asg017/inverted-nasa-photos note: if you have privacy badger you'll have to turn it off as it thinks any page calling a nasa.gov page that isn't a nasa.gov site is a spam site!
- How does ____ of artwork change over time? Can you see changes in colors or levels of contrast?
- Map artwork provenance with a set of data. Put it on a map. 
- What features are predictions of artwork size?
- Can you pull out geographic entities using SpaCy or other NLP tool from descriptions that aren't in provenance category?
- What are the most common first names of artists in each 50 year period?
- Use http://scikit-image.org/docs/dev/auto_examples/ to do something?
- When did high hue values within some subset of the data get most popular, <a href="http://scikit-image.org/docs/dev/auto_examples/color_exposure/plot_rgb_to_hsv.html#sphx-glr-auto-examples-color-exposure-plot-rgb-to-hsv-py">this is a possible starting point</a>.
- Find all the artwork descriptions that share an entity using <a href="https://spacy.io/">SpaCy</a>. 
- Can you find and visualize all the cats?

## Twitter handles & hashtags to share your visualizations with


## Attribution 
You may wish to attribute or cite The Cleveland Museum of Art CC0 select datasets, especially with respect to research or publication. Attribution is not required, but does support efforts to release other datasets in the future. It also helps to retain source links and reduce “orphaned data.”  

### Do not misrepresent the dataset
Do not mislead others or misrepresent the datasets or their source. You must not use The Cleveland Museum of Art’s trademarks or otherwise claim or imply that the Museum or any other third party endorses you or your use of the dataset. 

Whenever you transform, translate or otherwise modify the dataset, you must make it clear that the resulting information has been modified. If you enrich or otherwise modify the dataset, consider publishing the derived dataset without reuse restrictions. 




