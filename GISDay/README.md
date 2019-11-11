# Texas A&M GIS Day - GIS + Visualizations + Video Game Engines
#### by - Liam Lyle

## Requirements:
1. A basic understanding of how FME works
2. A basic understanding of GIS Principles (projections, coordinates, data)
3. A basic understanding of Video Games and 3D Engines
4. How to un-zip files + have organized folders

## Softwares:

Click on the links to download/get a free trial of application. More information can be found on the GIS Day website [here](https://gisday.tamu.edu/sessions/#/details/d3b3c7d3-7171-47a3-87b3-9ffb32405f37)

This workshop will require heavy computation and graphical work, so make sure to have a semi-beefy computer if you're going to follow along. My laptop specs: Intel i7, AMD Radeon (TM) R7 M460 Graphics Card, 16 GB RAM 
***

<p align="center"> <a href="https://store.unity.com/download-nuo">Unity - 2018/2019</a> </p>
<p align="center"> <img src="https://unity3d.com/files/images/ogimg.jpg" alt="unity" width="200" height="100"/> </p>

<p align="center"> <a href = "https://www.safe.com/">FME - 2019 </a> </p>
<p align="center"> <img src="https://yt3.ggpht.com/a/AGF-l78ddntvyWHDcTe2_VS0I9cZK74Z-_qcqP-qRg=s900-c-k-c0xffffffff-no-rj-mo" alt="FME" width="100" height="100"/> </p>

<p align="center"> <a href ="https://www.esri.com/en-us/arcgis/products/arcgis-pro/trial">ArcPro (If needed to visualize GIS Data) </a> </p>
<p align="center"> <img src="https://www.esri.com/content/dam/esrisites/en-us/common/icons/product-logos/ArcGIS-Pro.png" alt="ArcPro" width="100" height="100"/> </p>


## Data:
#### Structures Data: https://data-cstx.opendata.arcgis.com/datasets/structures/data
#### College Station Road Data: https://data-cstx.opendata.arcgis.com/datasets/streets
#### LIDAR Data (1GB File): https://s3.amazonaws.com/data.tnris.org/b6ea8e3a-c8b7-4d97-b4d1-4eb8172eb87d/resources/usgs17-70cm-brazos-freestone-robertson_3096301_lpc.zip

#### Unity Assets:
- Character: https://assetstore.unity.com/packages/3d/characters/humanoids/character-pack-free-sample-79870
- Infinity Terrain Tool: https://assetstore.unity.com/packages/tools/terrain/real-world-terrain-8752 - Do not purchase for this workshop. This is only for your reference if you'd like to make an investment.

## Step-By-Step:
1. Install FME Desktop, and Unity
2. Download Data from section above
3. Open FME:
4. Create **Readers** for Street Data (.shp), for Structure Data (.shp), and USGS LIDAR Data - usgs17-70cm_14RQU545885 (.LAZ)
5. Follow this image below using transformers.
>
![FME_Workflow]()

6. Create writer to an shp file.
7. Make connections like the ones below:
>
![FME_Writer]()

8. **Open Unity**
9 Create new Project (make sure it is 3D)
10. Make a new folder in the "Assets" folder, naming it SKP (or whatever you'd like).
11. From a file explorer, move (drag) your 2 made skp files you've created from your FME job to Unity.
12. Click and drag them to your "Scene"
13. Add in a Terrain asset for your character to walk on (https://docs.unity3d.com/Manual/terrain-UsingTerrains.html)
14. Go to Unity Store, and search for the Character Asset (https://assetstore.unity.com/packages/3d/characters/humanoids/character-pack-free-sample-79870).
15. Import this character in, and place it on your scene. Add a camera to it. Adjust.
16. **Play game**
17. You can now create your own models and add them in (LIDARs, TIN files, etc).
