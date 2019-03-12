# Social Media Analytics

## Unit 2: Visualizing Social Networks

### Taxonomy of Visualizations

- There are 4 types of visualizations, depending on their focus:
  1. Structural Visualizations
  2. Semantic Visualizations
  3. Temporal Visualizations
  4. Statistical Visualizations

#### Structural Visualization

- Focuses on the **structure** of the network, i.e. the **topology** of the graph that represents entities and relationships.
- **Two approaches**:
  - Node Link Diagrams
    - Easy to interpret
  - Matrix Oriented Methods
    - Make better use of limited area
  - Hybrid Techniques
- Some **high level properties** that the layout must satisfy are:
  - Positions of nodes and links in the diagram should facilitate **readability**.
  - Positions of nodes should help uncover inherent **clusterability** in the network.
  - Positions of nodes should create a **trustworthy representation** of the social network.
- To satisfy these high level properties, **layout algorithms** are formulated in terms of **low level properties**.
  - Widely used property: **proximity of nodes**
  - Another property: **readability**, ensured by minimal node overlaps and edge crossings
- An "**uninformative hairball**" is formed by unreadable graphs.

##### Node Link Technique

- **Actors** are **represented by nodes** taking geometric forms.
- **Relationships** are **represented as lines between nodes**.
- E.g. **Sociogram**
- **Geometric properties** such as colour, size, shape and thickness can be **used to encode different properties** of the network.
- The **main challenge** is placement and layout of nodes in an effective way. As the size and complexity of the network increase, this becomes more challenging.
- **Types of layouts:**
  - **Property based** layouts
    - Assign a **value** to a node as its **position** in a co-ordinate system.
    - **Simple to compute.**
    - **Help discover patterns** in the distribution of that property across the network.
  - **Force directed and energy based** layouts
    - Draws an **analogy** from the physical structure of rods and springs connecting spheres with links and nodes in a network.
    - Forces are **designed to satisfy low level properties** that guarantee minimal overlap of nodes and proximity of related nodes.
    - **Expensive to compute.**
    - Often result in a "**hairball**" due to the power law distribution.
  - **Spectral** layouts
    - Based on **spectral algebra** on key matrices that can be extracted from social structure.
    - E.g. **eigenvectors** of certain matrices.

##### Matrix Oriented Techniques

- Represent a social network via an explicit display of its **adjacency/incidence matrix**.
- Each link is represented as a **grid location** with catesian co-ordinates corresponding to its nodes.
- **Colour and opacity** can be used to represent important structural or semantic properties.
- They are **compact** and **overlap free**.
- It is **challenging to** enable users to **visually identify** local and global **structures**. Depends on how nodes are **ordered**.
- The **matrix should retain clusters** of nodes in close proximity. This has been addressed as a clustering problem.

##### Hybrid Techniques

- **Node link** techniques are **easy to interpret**, but **matrix oriented** techniques are **better with dense networks**. This has led to a number of hybrid techniques.
- **Adjacency matrices** are often **difficult to read**. It is **difficult to follow paths** between two actors. This problem is addressed by using a **hybrid matrix**, where a basic layer depicts an adjacency matrix while enabling path navigation on a different layer. Using **transportation maps** as metaphors, this visualization shows paths between multiple pairs of nodes in a readable manner.
- **Node-Trix** is a hybrid that depicts dense communities within a social network as an adjacency matrix and connects these within a node link diagram.

#### Semantic and Temporal Visualizations

- Instead of highlighting the **explicit structural relationships** in the data, these diagrams represent **high level attributes** and connections of nodes and links.
- Semantic visualization techniques include:
  - Ontology-based visualization
  - Temporal Visualization

##### Ontology-based Visualization

- **Ontologies** can be **used to represent** the **types of actors and relationships** in a social network.
- E.g. **Ontovis**, in which a typical node-link diagram is enhanced with a high level graphical representation of the ontology.
- An ontology is a graph who's **nodes represent node types** and **links represent types of representations**.
- An ontology may be **explicitly given or extracted from data**.
- The **goal** here is not to discover structure, but to discover the distribution of attributes of nodes and links.

##### Temporal Visualization

- Special type of semantic visualization.
- Social interaction is a **time dependant phenomenon**. Hence, it is **natural** to represent the temporal dimension using visual means.
- Handling the temporal dimension from a structural point of view alone is insufficient. A semantic approach is more suited.
- Time as a dimension deserves different treatment as compared to other data-specific node attributes.
- One of the challenges in representing time is the shortage of dimensions while representing a dynamic network in a 2D display.
- Since the actual structure of links is not explicitly shown, these visualizations do not suffer from clutter and are quite effective for dynamic networks.
- Two dynamic representations have been considered:
  - Flipbooks: nodes remain static and edges change over time.
  - Movies: Nodes move as relationships change.
- Mobivis:
  - Enhances an ontology-based visualization with an interactive time chart.
  - Time chart is a pixel-oriented metaphor that incorporates temporal information about actors in the network.
- PostHistory
  - 