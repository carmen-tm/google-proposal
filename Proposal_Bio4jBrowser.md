#Graphical browser for Bio4j model#
[*Link to the project page*](https://github.com/bio4j/gsoc14/wiki/graphical-browser-for-bio4j-model)

##Project##
Development of an interactive web-based tool that will allow users to intuitively explore the Bio4j domain model, getting details about both nodes/edges shaping the network as well as precise typing information in order to understanding the Bio4j structure and managing or querying it on an easier and more efficient way.

The technology used will be the proposed D3.js JavaScript library.

**Loading the data model** 

A representation of the **Bio4j data model** will be obtained though a **GraphSON**, a JSON-based format file returned from a HTTP REST service, that will be loaded into d3.js on a similar way to other [usual methods](https://github.com/mbostock/d3/wiki/Requests) as `d3.json()` or `d3.csv()`.

**Proposed User interface design**

All data describing the graph DB model could be loaded at once on the browser (it's a **small dataset** of nodes and edges to allow this, with around 200 and 100 elements respectively) in order to bring a first **whole picture** of all the info integrated up to date.

Layout wise, the platform will be defined graphically and functionally along the first working period of the project, but as first rough approach of what could be done, a two possibilities re-arrangement of the info could be offered to the users: 

- A basic first tryout could be a simple but functional radial node-link distribution layout centered on the Protein core node, as the most intuitive first approach to the domain model, where nodes are being distributed around without overlapping and all connections slightly displayed.
- A second rearrangement the network will be defined on a second stage, repositioning the nodes on a different way [(as on this case)](http://tulpinteractive.com/close-votes/) in order to offer the users a better sense of navigation along the domain model, or to explore intrinsic biological patterns or content depending on what info/connections are appearing/lacking related to certain protein.

On both cases, the nodes size could show the updated amount of data stored, and other relevant characteristics (existence and amount of nodes/edges properties, etc) could be communicated with any simple visual code.

The use of color could categorized the dataset from the beginning differentiating the main data sources of the database on the big main groups: *UniProtKB (SwissProt + Trembl), Gene Ontology (GO), UniRef (50, 90, 100), RefSeq, NCBI taxonomy, Expasy Enzyme*, although this could be redefined later.

While hovering on a specific node, all connecting nodes could be visually highlighted. The nature of the relationships (edges types as one to one, one to many, etc.) has a big importance on this project and should be solved consequently with an initial solution again through a different graphical display, although further solutions related to the user navigation and/or the nodes position will be explored. A lateral threshold limiting the number of steps to be highlighted could help to explore the relationships on a better way (as on this case, but highlighting more/less rather than showing/hiding) . This will allow users focusing operations without losing the context.

Additionally, **filtering on/off** operations of the main **sources of information groups** if no relevant for the user purposes could be allowed and would reposition filtered set spatially.

All **typing information** (indexes) will be displayed on the visualization. When clicking on a node, exploring its neighborhood, clicking on next one, and so on defining a certain path, all indexes could be showed on the lateral forming a indexes list for the specific route covered. As far as users navigate through the diagram nodes, the **pathways** will be outstanding graphically literally drawing the route, accompanied by the related **index list** for a further easy copy/paste operation with the Bio4j platform. This navigation will allow modifications on the path election dynamically.

Different possibilities of side-elements in order to help the visualization navigation will be explored (showing/hiding labels, transparency, etc), finally including just the most relevant ones, as usually more simple interfaces are in most cases smarter.

In my opinion, a graphical tool with a neat and worked graphical display, a simple but meaningful layout and a friendly and efficient interaction behavior will allow Bio4j’s users approach the platform on a nicer and effortless way.



##Work Plan##

General timing plan proposed, to be redefined more precisely:

**Phase0** From 2nd week March – 2nd week May     (2 months, partial dedication)

- JavaScript and d3 specifically self-taught learning period, through manuals and online resources.

- First contact with the Bio4j platform to get familiarized with it and know what kind of info has and it is requested by users.

- Collaboration on defining the JSON representation of the data model mentioned on the Project section.


**Phase1** From 3rd week May – 3rd week June     (1 month, full dedication)

- Platform initial settings (referencing d3, loading JSON data, etc)

- Concept design. Generation of sketches and diagrams

- Evaluation of better solutions and possibilities with the project mentors.

- Start coding the basic functionalities (Initial Layout mentioned on the Project section).

// 23-27 June // Mid-term evaluations period. Resume of project state uploaded to the GSoC platform


**Phase2** From 4th week June – 3rd week August     (2 months, full dedication)

- Revision of the project state. Suggestion of additional features and tweacks.

- Styling the visualization properties, Interactions and transitions behaviors.

- First Layout functionality complete and Evaluation.

- Coding the 2nd functionalities (Second Layout mentioned on the Project section).

- Revisions and implementations.

// 18-22 August // Final evaluations period. Final outcome uploaded to the GSoC platform



##Why Me##

Well…Let’s say I have an academic background as Architect, but I always find myself moving into other interdisciplinary fields, facing digital design processes of different nature, starting from but not limited to graphics or different kinds of visualizations.

 In general I find a special interest on anything that requires a mix of technical and creative skills. On the graphics field in particular I’ve always been curious about **data visualization possibilities** due its transversality and communication/storytelling capacities.

From university learning period I always put attention to anything related to maps and cartographies, and how they could communicate more than geographical information somehow… landing on more and more abstract diagrammatic representations mixing narrative, social, economic, geographic or subjective data… From that period belongs the [Reu08 Cartography project](http://ooopart.com/#see_modal_P1), as exploration of different representation languages and physical materials.

Professionally, my first experience with data came across the [River of Light-Sources installation (2010)](http://ooopart.com/#see_modal_S14) while at Creatmosphere lighting studio. Environmental data related to the Canadian Bow River was researched and communicated through printed cartographies, projections and motion and color lighting patterns on a floating light matrix as part of the temporary installation. As main researcher of the project, I discover an stimulating role as analyzer and visualizer on many possible exciting experiences.

From that moment I have participated on several similar experiences (like [here](http://ooopart.com/#see_modal_P2), [here](http://ooopart.com/#see_modal_S17) or [here](http://ooopart.com/#see_modal_P5)) in general with a strong **narrative focus** and different information sources (environmental, scientific, urban, historical, etc) but always with small datasets and either limited to static or simple dynamic representations or just defining the projects both conceptually and graphically but letting other people materializing them, which at the end has been problematic sometimes.

My knowledge is lacking among **text based programming language** or scripting, but I actually don’t find my methodologies far from its logics on my work related to visual representations and even more to 3d modeling specifically. I have full experience working and teaching [Grasshopper 3D](http://en.wikipedia.org/wiki/Grasshopper_3d), a **visual programming language** integrated on Rhino’s 3d CAD modeling tool, which at the end consists as well on setting all rules to generate a design system based on variable parameters and relationships.

I am aware of the important initial learning curve implicit on developing this project myself, and for that I am already investing my time on a pre-work **d3-javascript learning period** referred on the working plan above. I am starting with some **online resources** for learning d3.js as the Scott Murray’s [manual](http://chimera.labs.oreilly.com/books/1230000000345), and I have more material on the list to dive afterwards ([here](https://www.dashingd3js.com/table-of-contents) or [here](https://github.com/mbostock/d3/wiki/Tutorials)). On top, at the end of this learning period I will put all the knowledge achieved starting some first d3 simple visualizations for another project related to environmental data visualization (with this [organization](http://wiki.obsnev.es/index.php/P%C3%A1gina_principal)), which will give me some **extra experience** just before starting officially the work in middle May. During this period I might need the mentors help exceptionally if getting stuck, but it will happens rarely. I think the first contacts with the Bio4j database environment might require more support, as I guess I will find the mentioned user barrier when confronting it, specially because I don’t come from the bioinformatics field as other users do.



In resume, I see this project as a **unique opportunity** to learn basic code and explore the graphical and functional possibilities of programming interactive data interfaces, as the ideal way to communicate all sort of information empowering people to explore it dynamically by themselves.



Contact details:                                  

*carmen@ooopart.com*

*GitHub: carmen-ooo  /   Skype: carmen.torrecillas*

*Twitter: @ooopart   /   Mob: +34 622 226913*                                      






