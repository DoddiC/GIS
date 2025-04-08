**Core Functionality and Overview:**

*   **ArcGIS Pro is Esri's professional desktop GIS application**. It's designed for experienced GIS users and those looking to enhance their skills.
*   It supports a wide range of GIS tasks, including **managing data, creating cartographic outputs (maps and layouts), performing spatial analysis, and running geoprocessing tools**.
*   ArcGIS Pro aims to allow users to **tackle complex spatial data tasks**.
*   It is the **preferred language for working with ArcGIS Pro is Python**, which is strongly reflected in the software's functionality.
*   Python scripting in ArcGIS Pro allows you to **automate tasks that would be cumbersome using the regular menu-driven interface**. This includes automating workflows for data management, analysis, and map production.
*   ArcGIS Pro supports the use of scripting to **automate workflows**.
*   It provides access to **all the tools available in ArcGIS Pro, including those that are part of ArcGIS Pro extensions**, through the **ArcPy package**.
*   ArcGIS Pro works with **Python 3**, whereas ArcGIS Desktop 10.x worked with Python 2. Migrating scripts from Python 2 to 3 is a consideration.
*   Beyond ArcPy, ArcGIS Pro also supports the **ArcGIS API for Python** for working with **web GIS** (like ArcGIS Online and ArcGIS Enterprise). This allows for tasks such as creating maps, geocoding, and performing analysis on web-based data.
*   **Jupyter Notebook** is the recommended IDE for working with the ArcGIS API for Python and can be used directly within ArcGIS Pro.

**Geoprocessing Framework:**

*   The **geoprocessing framework** in ArcGIS Pro facilitates the sharing of tools.
*   There are **three main types of tools in ArcGIS Pro**:
    *   **Built-in tools**: These are created by Esri using ArcObjects and compiled programming languages. They are represented by a pathway model icon. Most tools in ArcGIS Pro are built-in.
    *   **Script tools**: These consist of Python scripts that are accessed through a tool dialog box. They can be created in a toolbox (.tbx) and reference a single Python script file (.py). Effective script tools have carefully designed parameters that define the tool dialog box. They are represented by a scroll icon. Built-in script tools written by Esri are indicated by a hammer icon.
    *   **Model tools**: These are created using ModelBuilder, a visual programming environment. A model can be exported to a Python script.
*   **Toolboxes (.tbx)** can contain any number of tools, including both model and script tools. A toolbox icon represents a toolbox. A toolset (a collection of related tools within a toolbox) is shown as a toolbox with a hammer. Python toolboxes are created entirely in Python and consist of a single .pyt file.
*   The **input and output of geoprocessing functions are called parameters**. Required and optional parameters are indicated in ArcGIS Pro and Esri documentation.
*   **ArcPy provides access to all geoprocessing tools**. The syntax for running a tool in Python is `arcpy.<toolname_toolboxalias>(<parameters>)`.
*   **Environment settings** can impact how geoprocessing tools run. These settings are passed from ArcGIS Pro to the tool.
*   **Batch processing** allows running a tool multiple times with different inputs.
*   **Custom tools** (script tools and Python toolboxes) allow for closer integration of scripts within the ArcGIS Pro geoprocessing framework and make it easier to share workflows with others who may not know Python.
*   **Web tools** can be authored and published from ArcGIS Pro, allowing for sharing analysis over the web.

**Python Scripting in ArcGIS Pro:**

*   **Python is the preferred scripting language** because it is simple, easy to learn, free, and open source. It also has a large user community and a growing set of third-party packages.
*   The **ArcPy package** is fundamental for geoprocessing in Python within ArcGIS Pro. To use it, you need to `import arcpy`.
*   ArcPy is organized into **modules, functions, and classes**. Geoprocessing tools are accessed as functions within ArcPy.
*   **Tool parameters** in Python scripts can be defined using variables instead of hard-coding values, making the code more versatile.
*   The **Result object** in ArcPy provides information about the execution of a geoprocessing tool, including messages.
*   **Python editors (IDEs)** are used to write and test scripts. Recommended editors include IDLE (installed with Python), Spyder, and potentially PyCharm. ArcGIS Pro uses a specific Python distribution, and it's important to use the Python environment associated with ArcGIS Pro.
*   The **Python window** within ArcGIS Pro allows for interactive execution of Python code and is integrated with the geoprocessing framework.
*   **ArcGIS Pro uses a specific Python environment** (`arcgispro-py3` by default) which includes necessary packages. Packages can be managed using the **Python Package Manager** in ArcGIS Pro or using **conda**.
*   **Third-party Python packages** can be used to extend the functionality of Python in ArcGIS Pro.

**ArcGIS API for Python:**

*   The ArcGIS API for Python is used to work with **web GIS** (ArcGIS Online and ArcGIS Enterprise) without needing to use ArcGIS Pro directly for all tasks.
*   It provides tools for tasks similar to ArcPy but designed for web environments, such as creating maps, geocoding, and managing data online.
*   Code for the ArcGIS API for Python is typically written in **Jupyter Notebooks**, which offer built-in visualization capabilities. Notebooks can also be used within ArcGIS Pro.
*   The ArcGIS API for Python is built on the **ArcGIS REST API**.
*   The main module of the ArcGIS API for Python is the **`gis` module**, which allows you to manage the content of your GIS, as well as users and their roles. The main class within this module is **`GIS`**, representing the GIS you are working with.
*   The `gis` object includes a **map widget** for visualization.

**Sharing Tools and Scripts:**

*   Custom tools (script tools and Python toolboxes) can be added to a project and integrated into regular workflows.
*   Script tools can be shared by distributing the toolbox file (.tbx) and the accompanying Python scripts (.py), along with any necessary data. Relative paths should be used to ensure tools work even if files are moved.
*   Python toolboxes (.pyt files) can be shared by distributing the .pyt file and any other required resources.
*   Tools and toolboxes can be documented by editing their metadata, including descriptions and parameter explanations. Separate documentation (manuals, user guides) can also be provided.
*   **Geoprocessing packages** can be created and shared.

**Key Concepts and Terminology (from the sources):**

*   **ArcPy**: The Python package for geoprocessing in ArcGIS Pro.
*   **ArcGIS API for Python**: The Python package for working with web GIS.
*   **Script tool**: A custom geoprocessing tool that runs a Python script.
*   **Python toolbox**: A collection of custom geoprocessing tools created entirely in Python.
*   **Toolbox**: A container for geoprocessing tools.
*   **Toolset**: A collection of related tools within a toolbox.
*   **Parameter**: Input or output of a geoprocessing function.
*   **Geoprocessing framework**: The architecture within ArcGIS Pro for executing and managing geoprocessing operations.
*   **Automation**: Using scripts or models to perform tasks automatically.
*   **Web GIS**: A distributed information system for storing, managing, visualizing, and analyzing geographic data on the web.
*   **Jupyter Notebook**: An open-source web application for creating and sharing documents with live code, equations, visualizations, and narrative text.
*   **Module**: A file containing Python definitions and statements. Examples include `arcpy`, `os`.
*   **Package**: A collection of Python modules organized under a common folder with an `__init__.py` file. `arcpy` is a package.
*   **Environment**: Settings that affect the execution of geoprocessing tools.
*   **Function**: A block of organized, reusable code that performs a specific action. Geoprocessing tools are accessed as functions in ArcPy.
*   **Class**: A blueprint for creating objects.

**Resources and Help:**

*   **ArcGIS Pro help pages**: Provide extensive documentation on tools, ArcPy, and other functionalities. You can access help by clicking the help icon in the tool dialog box.
*   The **ArcGIS Pro Python reference**: Located under the Python tab in the help pages, it documents all ArcPy functionality.
*   **Esri Press books**: Such as "Python Scripting for ArcGIS Pro" and "Advanced Python Scripting for ArcGIS Pro" provide comprehensive guidance and examples.
*   **ArcGIS Online resources and help documents**.
*   Online communities like **GIS Stack Exchange** and **GeoNet**.
*   The **Python documentation** at `http://www.python.org`.
*   **Esri's developer website** for the ArcGIS API for Python, including guides and samples: `https://developers.arcgis.com/python/guide/` and `https://developers.arcgis.com/python/samples/`.
*   The **CIM specification** is hosted on GitHub: `https://github.com/esri/cim-spec`.

This overview covers many of the key aspects of ArcGIS Pro relevant to its functionality, its integration with Python, and its use in geoprocessing and automation. It should provide a solid foundation for interview discussions and serve as a useful study guide. Remember to emphasize your practical experience with these concepts if you have any.

Here is a cheatsheet based on the ArcGIS Pro Manual:

**ArcGIS Pro Cheatsheet**

**Getting Started**

*   **Creating a New Project:** File > New > Map. Specify name and folder.
*   **Setting Units:** Project Tab > Options > Units. Choose units for distance, angle, area, location, and direction.
*   **Creating a New Map:** Insert Tab > New Map. Options for multiple maps, global/local scenes, stereo maps, and basemaps.
*   **Interface Elements:**
    *   **Ribbon:** Organized into tabs (e.g., Map, Insert, Analysis, Edit, Share) with groups of tools.
    *   **Panels:** Docked windows like **Contents** (layers) and **Geoprocessing** (tools). Can be moved and docked.

**Data**

*   **Adding Data:** Map Tab > Layer Group > Add Data. Supports vector, raster, and tables.
*   **Raster Pyramids:** Recommended to build when adding raster images to enhance performance.
*   **Vector Model:** Represents geographic features as points, lines, or polygons.
*   **Raster Model:** Represents geographic features as a grid of cells, where each cell has a value.

**Georeferencing an Image**

*   **Purpose:** Assign a spatial reference system to a digital image based on known coordinates.
*   **Adding Ungeoreferenced Image:** Map Tab > Layer Group > Add Data.
*   **Setting Coordinate System (SRS):** Imagery Tab > Georeference > Prepare Group > Set SRS. Select desired coordinate system.
*   **Georeferencing with Control Points:**
    *   **Add Control Points Tool:** Georeference Tab > Adjust Group. Click on a known point in the image ("From point"), then right-click and enter real-world coordinates ("To point").
    *   More control points increase accuracy.
    *   Save georeferencing changes: Georeference Tab > Save Group > Save or Save as New.
*   **Georeferencing Without Control Points:** Can be done using common points with an existing georeferenced vector layer.

**Creating and Editing Vector Entities**

*   **Creation of Feature Class (Shapefiles):** Analysis Tab > Geoprocessing > Tools. Search for "Create Feature Class". Define location, name, geometry type (point, line, polygon), and coordinate system.
*   **Editing Vector Layers:** Edit Tab.
    *   **Create Features Panel:** Edit Tab > Create. Select layer and geometry type to start digitizing.
    *   **Editing Points:** Select point layer, use "Point" template, click on the map. Can also insert XY coordinates using "Absolute X,Y". Use "Move" tool to adjust location.
    *   **Editing Lines:** Select line layer, use appropriate template, click to add vertices, double-click to finish. Use "Edit Vertices" tool to modify vertices.
    *   **Editing Polygons:** Select polygon layer, use appropriate template, click to add vertices, double-click to finish. Use "Edit Vertices" tool to modify vertices. "Autocomplete Polygon" tool for digitizing adjacent polygons.
    *   **Saving Edits:** Edit Tab > Manage Edits Group > Save.
    *   **Merging Polygons:** Select polygons (Shift + Select), Edit Tab > Tools > Merge.

**Table Management**

*   **Viewing Attribute Table:** Right-click layer in Contents panel > Attribute Table.
*   **Creating New Fields:** Open Attribute Table > Table Menu > Add. Configure Field Name, Data Type (e.g., Text, Double, Integer, Date), and Properties (e.g., Length, Precision, Scale).
*   **Entering Information:** Double-click on a cell to enter values.
*   **Calculating Field Values:** Select rows (optional), right-click on field > Calculate Field. Use Python, Arcade, or VBScript expressions. Can insert values from other fields.
*   **Calculating Area, Perimeter, and Length:** Ensure layer has a defined coordinate system. Use "Calculate Geometry" tool (right-click field > Calculate Geometry).
*   **Calculating XY Coordinates:** Use "Add Geometry Attributes" tool (Analysis > Tools) for point layers.
*   **Operations:** "Calculate Field" allows for mathematical and text string operations.

**Design and Publication**

*   **Symbology:** Right-click layer > Symbology.
    *   **Single symbol, Unique values, Graduated colors, Graduated symbols, Charts, Dictionary, Heat map**.
    *   Customize symbols: Double-click symbol in Contents > Symbology Panel > Gallery or Properties. Adjust color, size, width, outline.
*   **Labels:** Select layer > Labeling Tab.
    *   Activate "Label" button, choose label field.
    *   **Simple Labels:** Configure text symbol (font, size, color).
    *   **Combined Labels:** Use "Expression" to combine multiple fields or add text.
    *   **Labels of a Specific Category:** Define label classes with specific conditions.
*   **Map Layout:** Insert Tab > New Layout. Choose orientation and paper size.
    *   **Map Body (Map Frame):** Insert Tab > Map Frames > Select Map. Draw on layout.
    *   **Graticules (Coordinate Grid):** Select Map Frame > Element Panel > Grid > Add. Customize components (gridlines, ticks, labels, intersection points).
    *   **North Arrow:** Insert Tab > Map Surrounds > North Arrow.
    *   **Location Map:** Create a new map with broader extent, add to layout as another Map Frame, use "Extent Indicator" to show study area.
    *   **Legend:** Insert Tab > Map Surrounds > Legend. Customize title and elements in Element and Contents panels.
    *   **Numerical Scale:** Insert Tab > Graphics and Text > Dynamic Text > Scale.
    *   **Graphic Scale (Scale Bar):** Insert Tab > Map Surrounds > Scale Bar. Customize divisions and fitting strategy.
    *   **Geodetic Reference Parameters:** Insert Tab > Graphics and Text > Straight Text.
    *   **Card Area or Boxes:** Add text boxes (Insert > Graphics and Text), tables (Insert > Map Surrounds > Table Frame), and graphics (Insert > Graphics and Text > Graphic).
*   **Exporting and Printing a Map:** Share Tab > Output Group > Print Layout or Export Layout. Choose format (PDF, PNG, JPEG, etc.) and configure parameters.

**Geoprocessing Tools**

*   Access via Analysis Tab > Geoprocessing > Tools or Geoprocessing Panel.
*   Each tool requires input and output files and configurable fields.
*   **Areas of influence (Buffer):** Analysis > Tools > Buffer. Creates polygons around input features at a specified distance.
*   **Intersections (Intersect):** Analysis > Tools > Intersect. Creates new features where input features overlap.
*   **Clippings (Clip):** Analysis > Tools > Clip. Extracts features from an input layer that lie within the boundaries of a clip layer.
*   **Merge:** Geoprocessing > Toolboxes > Data Management Tools > General > Merge. Combines multiple layers of the same geometry type into one.
*   **Dissolve:** Geoprocessing > Toolboxes > Data Management Tools > Generalization > Dissolve. Aggregates features based on identical attribute values.
*   **Define Projection:** Geoprocessing > Toolboxes > Data Management Tools > Projections and Transformations > Define Projection. Assigns a coordinate system to a layer.
*   **Project a Layer:** Geoprocessing > Toolboxes > Data Management Tools > Projections and Transformations > Project. Transforms a layer from one coordinate system to another.

**Spatial Analysis**

*   **Interpolations:** Analysis > Tools > Interpolation Toolset. Estimate values at unsampled locations based on known values.
    *   **Importing XY Coordinates:** Map > Add Data > XY Point Data.
    *   **Interpolating Data (Kriging, IDW, Spline):** Geoprocessing > Toolboxes > Spatial Analyst Tools > Interpolation.
*   **Digital Elevation Models (DEM):** Raster dataset representing terrain elevation.
*   **Creation of slope maps:** Geoprocessing > Toolboxes > Spatial Analyst Tools > Surface > Slope. Calculates the rate of change in elevation.
*   **Reclassifications:** Geoprocessing > Toolboxes > Spatial Analyst Tools > Reclass > Reclassify. Changes raster values based on a defined scheme.
*   **Generation of Contours (Contour Lines):** Geoprocessing > Toolboxes > Spatial Analyst Tools > Surface > Contour. Creates lines connecting points of equal elevation.
*   **Hillshade Map:** Geoprocessing > Toolboxes > Spatial Analyst Tools > Surface > Hillshade. Creates a shaded relief map from a DEM.
*   **Viewshed:** Geoprocessing > Toolboxes > Spatial Analyst Tools > Visibility > Geodesic Viewshed. Determines areas visible from a specific point.
*   **Map Algebra (Raster Calculator):** Map Algebra pane or Geoprocessing > Toolboxes > Spatial Analyst Tools > Map Algebra > Raster Calculator. Performs mathematical operations on raster layers.
*   **Delineation of a Watershed:** Geoprocessing > Toolboxes > Spatial Analyst Tools > Hydrology. Identifies the drainage area upstream of a point. (Fill, Flow Direction, Flow Accumulation, Stream Order, Stream to Feature, Snap Pour Point, Watershed).
*   **Geoprocessing Automation with "ModelBuilder":** Analysis Tab > Geoprocessing > ModelBuilder. Creates workflows by connecting geoprocessing tools.
*   **Topographic Profiles:** Right-click raster layer > Create Chart > Profile. Displays elevation changes along a line.

**Image Analysis**

*   **Adding a Satellite Image from "Basemap":** Map Tab > Layer > Basemap.
*   **Downloading Landsat Images:** Via USGS Earth Explorer website.
*   **Download images Sentinel 2:** Via Copernicus Open Access Hub.
*   **Combining Satellite Image Bands:** Display different bands in RGB channels. Add multispectral image directly (ArcGIS Pro >= 3.2).
*   **Calculating NDVI:** Imagery Tab > Indices Group > NDVI. Measures vegetation health and density.

**Graphics**

*   **Creating a Histogram:** Right-click layer (raster or feature with attribute) > Create Chart > Histogram.
*   **Charts from Tables:** Right-click table in Contents > Create Chart. Various chart types available (bar, line, scatter, etc.).
*   **Spectral Signature Charts:** Right-click multispectral image > Create Chart > Spectral Profile. Displays spectral reflectance across different bands for selected areas.

**3D View**

*   Create 3D scenes from 2D data.
*   Elevation surfaces manage vertical positioning.
*   Create animations using bookmarks (View > Animation).

**Geodatabases**

*   Centralized container for managing geospatial data. Created automatically with a new project. Can create new ones in Catalog View.
*   **Creating and Configuring Domains:** Right-click geodatabase > Domains. Define allowed values for attribute fields.
*   **Create and Manage a "Feature Dataset":** Right-click geodatabase > New > Feature Dataset. Organizes related feature classes.
*   **Creating and Managing "Feature Class":** Right-click Feature Dataset > New > Feature Class. Define name, geometry type, fields, and assign domains.
*   **Importing Information from a "Shapefile" to a "Feature Class":** Right-click Feature Class > Load > Load Data (Append tool). Match fields between shapefile and feature class.
*   **Configuring Tables Based on Domains:** Load layer from geodatabase, open attribute table, enter domain codes to display descriptions.

**Topology**

*   Rules and spatial relationships between features within a geodatabase. Ensures data integrity.
*   **Defining Topological Rules:** In Catalog View, right-click Feature Dataset > New > Topology. Select participating feature classes and define rules (e.g., Must Not Overlap, Must Not Have Dangles).
*   **Identification and Correction of Errors:** Right-click topology > Validate. Use Error Inspector to identify and fix errors using various tools (e.g., Reshape Feature, Extend).
*   **Validation:** After correction, revalidate the topology.

This cheatsheet provides a summary of key concepts and steps in ArcGIS Pro based on the provided manual. Remember to refer to the manual for more detailed information and specific instructions.

ArcGIS Pro: A Practical Cheatsheet
Here is a cheatsheet based on the ArcGIS Pro Manual:
ArcGIS Pro Cheatsheet
Getting Started
•
Creating a New Project: File > New > Map [1, 2]. Specify name and folder [2].
•
Setting Units: Project Tab > Options > Units [3, 4]. Choose units for distance, angle, area, location, and direction [3].
•
Creating a New Map: Insert Tab > New Map [4]. Options for multiple maps, global/local scenes, stereo maps, and basemaps [4].
•
Interface Elements:
◦
Ribbon: Organized into tabs (e.g., Map, Insert, Analysis, Edit, Share) with groups of tools [5, 6].
◦
Panels: Docked windows like Contents (layers) and Geoprocessing (tools) [7]. Can be moved and docked [8].
Data
•
Adding Data: Map Tab > Layer Group > Add Data [9]. Supports vector, raster, and tables [10].
•
Raster Pyramids: Recommended to build when adding raster images to enhance performance [10, 11].
•
Vector Model: Represents geographic features as points, lines, or polygons [1].
•
Raster Model: Represents geographic features as a grid of cells, where each cell has a value [1].
Georeferencing an Image
•
Purpose: Assign a spatial reference system to a digital image based on known coordinates [8].
•
Adding Ungeoreferenced Image: Map Tab > Layer Group > Add Data [9].
•
Setting Coordinate System (SRS): Imagery Tab > Georeference > Prepare Group > Set SRS [12, 13]. Select desired coordinate system [13].
•
Georeferencing with Control Points:
◦
Add Control Points Tool: Georeference Tab > Adjust Group [14]. Click on a known point in the image ("From point"), then right-click and enter real-world coordinates ("To point") [15].
◦
More control points increase accuracy [16].
◦
Save georeferencing changes: Georeference Tab > Save Group > Save or Save as New [17].
•
Georeferencing Without Control Points: Can be done using common points with an existing georeferenced vector layer [18, 19].
Creating and Editing Vector Entities
•
Creation of Feature Class (Shapefiles): Analysis Tab > Geoprocessing > Tools [20]. Search for "Create Feature Class" [21]. Define location, name, geometry type (point, line, polygon), and coordinate system [22-24].
•
Editing Vector Layers: Edit Tab [25, 26].
◦
Create Features Panel: Edit Tab > Create [27]. Select layer and geometry type to start digitizing [28].
◦
Editing Points: Select point layer, use "Point" template, click on the map [28]. Can also insert XY coordinates using "Absolute X,Y" [29, 30]. Use "Move" tool to adjust location [31].
◦
Editing Lines: Select line layer, use appropriate template, click to add vertices, double-click to finish [31]. Use "Edit Vertices" tool to modify vertices [32].
◦
Editing Polygons: Select polygon layer, use appropriate template, click to add vertices, double-click to finish [32]. Use "Edit Vertices" tool to modify vertices [32]. "Autocomplete Polygon" tool for digitizing adjacent polygons [33].
◦
Saving Edits: Edit Tab > Manage Edits Group > Save [26].
◦
Merging Polygons: Select polygons (Shift + Select), Edit Tab > Tools > Merge [33].
Table Management
•
Viewing Attribute Table: Right-click layer in Contents panel > Attribute Table [34].
•
Creating New Fields: Open Attribute Table > Table Menu > Add [34]. Configure Field Name, Data Type (e.g., Text, Double, Integer, Date), and Properties (e.g., Length, Precision, Scale) [34, 35].
•
Entering Information: Double-click on a cell to enter values [35].
•
Calculating Field Values: Select rows (optional), right-click on field > Calculate Field [36]. Use Python, Arcade, or VBScript expressions [36, 37]. Can insert values from other fields [37].
•
Calculating Area, Perimeter, and Length: Ensure layer has a defined coordinate system [38]. Use "Calculate Geometry" tool (right-click field > Calculate Geometry) [38, 39].
•
Calculating XY Coordinates: Use "Add Geometry Attributes" tool (Analysis > Tools) for point layers [39].
•
Operations: "Calculate Field" allows for mathematical and text string operations [39].
Design and Publication
•
Symbology: Right-click layer > Symbology [40].
◦
Single symbol, Unique values, Graduated colors, Graduated symbols, Charts, Dictionary, Heat map [40, 41].
◦
Customize symbols: Double-click symbol in Contents > Symbology Panel > Gallery or Properties [42, 43]. Adjust color, size, width, outline [43, 44].
•
Labels: Select layer > Labeling Tab [45].
◦
Activate "Label" button, choose label field [45].
◦
Simple Labels: Configure text symbol (font, size, color) [46].
◦
Combined Labels: Use "Expression" to combine multiple fields or add text [46].
◦
Labels of a Specific Category: Define label classes with specific conditions [46].
•
Map Layout: Insert Tab > New Layout [47]. Choose orientation and paper size [47].
◦
Map Body (Map Frame): Insert Tab > Map Frames > Select Map [48]. Draw on layout [48].
◦
Graticules (Coordinate Grid): Select Map Frame > Element Panel > Grid > Add [49]. Customize components (gridlines, ticks, labels, intersection points) [49, 50].
◦
North Arrow: Insert Tab > Map Surrounds > North Arrow [50].
◦
Location Map: Create a new map with broader extent, add to layout as another Map Frame, use "Extent Indicator" to show study area [51-53].
◦
Legend: Insert Tab > Map Surrounds > Legend [54, 55]. Customize title and elements in Element and Contents panels [55, 56].
◦
Numerical Scale: Insert Tab > Graphics and Text > Dynamic Text > Scale [57].
◦
Graphic Scale (Scale Bar): Insert Tab > Map Surrounds > Scale Bar [57, 58]. Customize divisions and fitting strategy [58].
◦
Geodetic Reference Parameters: Insert Tab > Graphics and Text > Straight Text [59].
◦
Card Area or Boxes: Add text boxes (Insert > Graphics and Text), tables (Insert > Map Surrounds > Table Frame), and graphics (Insert > Graphics and Text > Graphic) [59-62].
•
Exporting and Printing a Map: Share Tab > Output Group > Print Layout or Export Layout [63, 64]. Choose format (PDF, PNG, JPEG, etc.) and configure parameters [64, 65].
Geoprocessing Tools
•
Access via Analysis Tab > Geoprocessing > Tools or Geoprocessing Panel [20, 21].
•
Each tool requires input and output files and configurable fields [66].
•
Areas of influence (Buffer): Analysis > Tools > Buffer [67]. Creates polygons around input features at a specified distance [67].
•
Intersections (Intersect): Analysis > Tools > Intersect [67]. Creates new features where input features overlap [67].
•
Clippings (Clip): Analysis > Tools > Clip [67, 68]. Extracts features from an input layer that lie within the boundaries of a clip layer [68].
•
Merge: Geoprocessing > Toolboxes > Data Management Tools > General > Merge [67, 69]. Combines multiple layers of the same geometry type into one [69].
•
Dissolve: Geoprocessing > Toolboxes > Data Management Tools > Generalization > Dissolve [67, 70, 71]. Aggregates features based on identical attribute values [70].
•
Define Projection: Geoprocessing > Toolboxes > Data Management Tools > Projections and Transformations > Define Projection [67]. Assigns a coordinate system to a layer [67].
•
Project a Layer: Geoprocessing > Toolboxes > Data Management Tools > Projections and Transformations > Project [72, 73]. Transforms a layer from one coordinate system to another [72, 73].
Spatial Analysis
•
Interpolations: Analysis > Tools > Interpolation Toolset [72, 74]. Estimate values at unsampled locations based on known values [72, 73].
◦
Importing XY Coordinates: Map > Add Data > XY Point Data [75].
◦
Interpolating Data (Kriging, IDW, Spline): Geoprocessing > Toolboxes > Spatial Analyst Tools > Interpolation [72, 74, 76].
•
Digital Elevation Models (DEM): Raster dataset representing terrain elevation [72].
•
Creation of slope maps: Geoprocessing > Toolboxes > Spatial Analyst Tools > Surface > Slope [72, 77]. Calculates the rate of change in elevation [72, 77].
•
Reclassifications: Geoprocessing > Toolboxes > Spatial Analyst Tools > Reclass > Reclassify [72, 78]. Changes raster values based on a defined scheme [72, 78].
•
Generation of Contours (Contour Lines): Geoprocessing > Toolboxes > Spatial Analyst Tools > Surface > Contour [72]. Creates lines connecting points of equal elevation [72].
•
Hillshade Map: Geoprocessing > Toolboxes > Spatial Analyst Tools > Surface > Hillshade [72, 79, 80]. Creates a shaded relief map from a DEM [72, 79, 80].
•
Viewshed: Geoprocessing > Toolboxes > Spatial Analyst Tools > Visibility > Geodesic Viewshed [72, 81, 82]. Determines areas visible from a specific point [72, 81, 82].
•
Map Algebra (Raster Calculator): Map Algebra pane or Geoprocessing > Toolboxes > Spatial Analyst Tools > Map Algebra > Raster Calculator [72, 74, 82, 83]. Performs mathematical operations on raster layers [72, 82, 83].
•
Delineation of a Watershed: Geoprocessing > Toolboxes > Spatial Analyst Tools > Hydrology [72, 84]. Identifies the drainage area upstream of a point [72, 84-88]. (Fill, Flow Direction, Flow Accumulation, Stream Order, Stream to Feature, Snap Pour Point, Watershed) [84-88].
•
Geoprocessing Automation with "ModelBuilder": Analysis Tab > Geoprocessing > ModelBuilder [72, 89]. Creates workflows by connecting geoprocessing tools [72, 89-92].
•
Topographic Profiles: Right-click raster layer > Create Chart > Profile [93-95]. Displays elevation changes along a line [93-95].
Image Analysis
•
Adding a Satellite Image from "Basemap": Map Tab > Layer > Basemap [93, 96, 97].
•
Downloading Landsat Images: Via USGS Earth Explorer website [93, 98, 99].
•
Download images Sentinel 2: Via Copernicus Open Access Hub [93, 100, 101].
•
Combining Satellite Image Bands: Display different bands in RGB channels [93, 102, 103]. Add multispectral image directly (ArcGIS Pro >= 3.2) [103].
•
Calculating NDVI: Imagery Tab > Indices Group > NDVI [93, 104]. Measures vegetation health and density [93, 104].
Graphics
•
Creating a Histogram: Right-click layer (raster or feature with attribute) > Create Chart > Histogram [93, 105].
•
Charts from Tables: Right-click table in Contents > Create Chart [93, 106]. Various chart types available (bar, line, scatter, etc.) [106, 107].
•
Spectral Signature Charts: Right-click multispectral image > Create Chart > Spectral Profile [93, 108]. Displays spectral reflectance across different bands for selected areas [93, 108, 109].
3D View
•
Create 3D scenes from 2D data [110-112].
•
Elevation surfaces manage vertical positioning [113].
•
Create animations using bookmarks (View > Animation) [113, 114].
Geodatabases
•
Centralized container for managing geospatial data [110, 114, 115]. Created automatically with a new project [115]. Can create new ones in Catalog View [115, 116].
•
Creating and Configuring Domains: Right-click geodatabase > Domains [110, 116, 117]. Define allowed values for attribute fields [110, 116, 117].
•
Create and Manage a "Feature Dataset": Right-click geodatabase > New > Feature Dataset [110, 118, 119]. Organizes related feature classes [110, 118, 119].
•
Creating and Managing "Feature Class": Right-click Feature Dataset > New > Feature Class [110, 120, 121]. Define name, geometry type, fields, and assign domains [110, 120, 121].
•
Importing Information from a "Shapefile" to a "Feature Class": Right-click Feature Class > Load > Load Data (Append tool) [110, 122, 123]. Match fields between shapefile and feature class [123, 124].
•
Configuring Tables Based on Domains: Load layer from geodatabase, open attribute table, enter domain codes to display descriptions [110, 125-127].
Topology
•
Rules and spatial relationships between features within a geodatabase [110, 128]. Ensures data integrity [110, 128].
•
Defining Topological Rules: In Catalog View, right-click Feature Dataset > New > Topology [129, 130]. Select participating feature classes and define rules (e.g., Must Not Overlap, Must Not Have Dangles) [130].
•
Identification and Correction of Errors: Right-click topology > Validate. Use Error Inspector to identify and fix errors using various tools (e.g., Reshape Feature, Extend) [110, 130, 131].
•
Validation: After correction, revalidate the topology [110, 131].