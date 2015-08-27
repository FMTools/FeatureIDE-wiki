<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/tthuem/FeatureIDE/wiki/Software-Product-Line-Developer)

<!-- Introduction -->
under construction

<!-- Outline -->

<!-- Content -->
- Feature Model Editor, graphical and text based.
   - Highlighting of dead and false-optional features and their corresponding constraints based on Sat4j.
   - Constraint Editor with content assist, syntax, and semantic checking, e.g., dead feature detection.
- Abstraction from the SPL source code for several outline and navigation tools, among others and overview how mixins are composed and which methods are present in previous features.
- Configuration Editor to create and edit configurations and with support for deriving valid configuration.
- Support for edits on feature models, i.e., categorizing edits into refactorings, generalizations, specializations or none of these.
- A view displaying statistics about the software product line.
- Feature-oriented programming:
   - Integration of AHEAD
   - Integration of FeatureC++
   - Integration of FeatureHouse with support for C, C#, Java 1.5, JML, Haskell, XML, JavaCC, ...
      - Family-based type checks with Fuji
- Aspect-oriented programming:
   - Integration of AspectJ
- Delta-oriented programming:
   - Integration of DeltaJ
   - Integration of DeltaEcore
- Annotation-based:
   - Integration of the C preprocessor with Colligens
      - Family-based type checks with TypeChef
   - Integration of the preprocessor Munge
   - Integration of the preprocessor Antenna
- Generation of all program variants
   - T-Wise variant generation with SPLCATool (including CASA)
-Support for feature model grammars of following tools:
   - The guidsl Tool, S.P.L.O.T., Velvet, fmp: Feature Modeling Plug-in, SPL Conqueror
   - Export of cnf in dimacs format.

[We also support colors](https://github.com/tthuem/FeatureIDE/wiki/Coloration)

For a detailed list of the main functionalities you can have a look at this [screenshots and videos](http://wwwiti.cs.uni-magdeburg.de/iti_db/research/featureide/#screenshots).

