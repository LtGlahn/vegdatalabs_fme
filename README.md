# OBSOLETE - check out [Nvdbapi_v2_FME](https://github.com/LtGlahn/Nvdbapi_v2_FME) 

> These routines are no longer active maintained, and V1 of NVDB api will eventually be scrapped. See [documentation for V2](https://www.vegvesen.no/nvdb/apidokumentasjon/) of NVDB api

Check out these alternatives: 
 * Generic routines @jetgeo for reading NVDB road network and NVDB objects from NVDB api v2 and save as GML. [NvdbGML](https://github.com/jetgeo/NVDBGML/tree/master/FME)
 * Simple routines for reading NVDB objects into FME workspace for a few selected object types. A little more handwork required to extend the functionality to other NVDB objects [Nvdbapi_v2_FME](https://github.com/LtGlahn/Nvdbapi_v2_FME) 

============


vegdatalabs_fme
===============

Introductory material and examples for reading data from the Norwegian Road database api (REST interface) https://www.vegvesen.no/nvdb/api/. Contains @LtGlahns presentation at #FMEWT (FME world tour) 6.5.2014, Oslo, and some sample FME workspaces. 
The presentation should provide valuable clues and hints about how to get started with the example work spaces. Please note that the location of the xfsmap definition file (*xfmapDefintion_nvdbapi2fme.xml*) in the XMLFeatureReader transformer must be adjusted to match your local file system.


Made with FME desktop 2014, seems to work fine in 2015.1.1, too. (Thanks to Ken Bragg @ safe.com for testing).


# FMEWT_simplestExample and FMEWT_apisearch.fmw

Make sure the location of the xfsmap defintion file (*xfmapDefintion_nvdbapi2fme.xml*) in the XMLFeatureReader transformer matches your local file system. 


# FMEWT_genericExample.fmw

In CSV reader, the  path to *attributeNames.csv* must be valid on your file system. Also, make sure the xfsmap defintion file (*xfmapDefintion_nvdbapi2fme.xml*) in the *XMLFeatureReader* transformer matches your local file system. 


# FMEWT_recursiveExample.fmw

As with **FMEWT_genericExample.fmw**, match the paths to *attributeNames.csv* and *xfsmap* definition file. 

You have to move the custom transformer definition file **Fetch_NVDB_objects.fmx** where your FME installation expects to find it. [Instructions at safe.com](https://knowledge.safe.com/articles/FAQ/How-Do-I-Install-a-Custom-Transformer)

FME evangelist on [custom transformers](https://blog.safe.com/2011/08/fmeevangelist87/)

[This is why](https://knowledge.safe.com/articles/Samples_and_Demos/Looping-with-Blocking-Transformers) I had to make an external custom transformer. 
