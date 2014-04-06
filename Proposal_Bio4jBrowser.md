#Graphical browser for Bio4j model#
[*Link to the project page*](https://github.com/bio4j/gsoc14/wiki/graphical-browser-for-bio4j-model)

##Project##
Development of an interactive web-based tool that will allow users to intuitively explore the Bio4j domain model, getting details about both nodes/edges shaping the network as well as precise typing information in order to understand the Bio4j structure and manage/query it on an easier and more efficient way.

The technology used will be the proposed D3.js JavaScript library.

**Loading the data model** 

A representation of the **Bio4j data model** will be obtained from **GraphSON** data, a JSON-based format file returned from a HTTP REST service that will be loaded into d3.js on a similar way to other [usual methods](https://github.com/mbostock/d3/wiki/Requests) as `d3.json()` or `d3.csv()`.

**Proposed User interface design**

All data describing the graph DB model will be loaded at once on the browser (it is a **small dataset** of nodes and edges so it does allow it) in order to bring a first **whole picture** of all the info integrated up to date.

Layout wise, I will work on a two-possibilities layout:

1. A **first basic network representation**. Simple but functional radial node-link distribution layout with SVG objects centered on the Protein core node, displaying slightly all connections without nodes overlapping.
2. A **second optional rearrangement** of the network will be defined on a second stage of the project in order to offer the users a better sense of navigation along the domain model, and to explore intrinsic biological patterns or content depending on what info/connections are appearing/lacking related to certain protein.

The first basic network representation will have the following characteristics:

- Nodes **sizes** showing the updated amount of data stored on them and other relevant characteristics showed thanks to a simple visual code.
- Use of **color** categorizing the dataset with the main data sources of the domain model on the big main groups: *UniProtKB (SwissProt + Trembl), Gene Ontology (GO), UniRef (50, 90, 100), RefSeq, NCBI taxonomy, Expasy Enzyme*.
- **Hover/click** interactions on nodes highlighting nodes connections or other behaviors. Edges types (one to one, one to many, self-linking nodes...) has a big importance on this project, and will be worked visually. 
- **Threshold** limiting the number of steps to be highlighted could help to explore the relationships on a better way (as on [this case](http://www.jasondavies.com/collatz-graph/), but highlighting more/less rather than showing/hiding) . This will allow users focusing operations without losing the context.
- **Filtering** operations of newtork through the main data sources groups or other relevant keys for the user proposes.
- Lateral menu with all **indexes/typing information** will be displayed. When clicking on a node, exploring its neighborhood, clicking on next one, and so on defining a certain path, all indexes will be listed for each specific route covered for a further easy copy/paste operation with the Bio4j platform.
- **Path drawing** as far as users navigate through the diagram nodes by clicking on the nodes consecutively. The pathways will highlighted graphically drawing the route accompanying the related index list mentioned above.

In my opinion, this first tryout with a basic network representation will be a very useful starting point to the project objectives during the Plase1 of the project referenced on the Work Plan below, as it will include the whole dataset and all basic functionalities that will allow Bio4j's users a nicer and effortless approach to the database. A second implemented layout could be developed based on this simple first approach during the Phase2 referenced below.


##Work Plan##


**Phase0. From 2nd week March – 2nd week May**     (2 months, partial dedication)

- D3 self-learning period through on-line resources.
- Familiarization with Github platform and MarkDown tool.
- Collaboration on defining the GraphSON representation of the data model.
- For 21 April: Test representation of a small part of the domain model as first contact with the Bio4j platform and the GraphSON data on d3. Basic network representation with SVG objects using the force-directed [Force layout](https://github.com/mbostock/d3/wiki/Force-Layout) implementation as simple first exploration.


**Phase1. From 3rd week May – 3rd week June**     (1 month, full dedication)

- First basic network layout concept re-design taking the d3-test mentioned above as starting point.
- Complete GraphSON dataset to be loaded properly on the model.
- Coding of all basic functionalities, including the whole set of nodes representation, nodes/edges properties display and edges variety differentiation.
- Revision with the project mentors and modifications based on that.
- For 23-27 June: **Mid-term evaluations period**. The resume of the project state will be uploaded to the GSoC platform.


**Phase2. From 4th week June – 3rd week August**    (2 months, full dedication)

- Revision of the project state and possible implementations list. 
- Optional: second layout concept design and main functionalities list. 
- Optional: codding of all basic functionalities of the second layout.
- Optional: creation of a new d3 component for working with graphSON data.
- Revisions with the project mentors and modifications based on that.
- For 18-22 August: **Final evaluations period**. The final outcomes will be uploaded to the GSoC platform.


**Work practices**: Communication with mentors along the phases through the following [github repository](https://github.com/carmen-ooo/google-proposal) and regular meetings.

##Why Me##

Well… I have an academic background as Architect, but I always find myself moving into other interdisciplinary fields, facing digital design processes of different nature, starting from but not limited to graphics or different kinds of visualizations. In general I am always interested on anything that requires a mix of technical and creative skills. On the graphics field in particular I have always been curious about the **data visualization possibilities** due its transversality and communication/storytelling capacities.

From **university learning period** I always put attention to maps and cartographies and how they could communicate more than geographical information somehow… landing on more and more abstract diagrammatic representations mixing narrative, social, economic, geographic or subjective data… From that period belongs the [Reu08 Cartography project](http://ooopart.com/#see_modal_P1), as exploration of different representation languages and physical materials.

My first **professional experience** with data came across the [River of Light-Sources installation (2010)](http://ooopart.com/#see_modal_S14) while at Creatmosphere lighting studio. Environmental data related to the Canadian Bow River was researched and communicated through printed cartographies, projections and motion/color lighting patterns on a floating light matrix as part of the temporary installation. As main researcher of the project, I discover an stimulating role as analyzer and visualizer on many possible exciting experiences. From that moment I have participated on other similar projects (like [here](http://ooopart.com/#see_modal_P2), [here](http://ooopart.com/#see_modal_S17) or [here](http://ooopart.com/#see_modal_P5)) in general with a strong **narrative focus** and different information sources but always working with small datasets and either limited to static representations or just defining the projects both conceptually and graphically but letting other people materializing them, which at the end has been sometimes problematic.

My knowledge is lacking among **text based programming language** or scripting, but I actually do not find my methodologies far from its logics on my work related to visual representations and even more to 3d modeling specifically. I have full experience working and teaching [Grasshopper 3D](http://en.wikipedia.org/wiki/Grasshopper_3d), a **visual programming language** integrated on Rhino’s 3d CAD modeling tool, which at the end consists as well on setting all rules to generate a design system based on variable parameters and relationships.

I am aware of the important initial learning curve implicit on developing this project myself, and for that I am already investing my time on a pre-work **d3-javascript learning period** referred on the working plan above, starting with some **online resources** for learning d3.js as this Scott Murray’s [basic manual](http://chimera.labs.oreilly.com/books/1230000000345) and other materials to dive afterwards ([here](https://www.dashingd3js.com/table-of-contents) or [here](https://github.com/mbostock/d3/wiki/Tutorials). Along this learning period I will start performing some test visualizations with environmental data for this [organization](http://wiki.obsnev.es/index.php/P%C3%A1gina_principal) to achieve some more extra experience before starting officially the project. During this period I might need the mentors help rarely if getting stuck, but I think the first contacts with the Bio4j database environment might require a bit more support.


In resume, I see this project as an **unique opportunity** to learn basic code and explore the graphical and functional possibilities of programming interactive data interfaces, as the ideal way to communicate certain information allowing the people to explore it dynamically.



Contact details:                                  

*carmen@ooopart.com*

*GitHub: carmen-ooo  /   Skype: carmen.torrecillas*

*Twitter: @ooopart   /   Mob: +34 622 226913*                                      






