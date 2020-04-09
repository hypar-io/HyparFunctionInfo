**JSON To Model converts Hypar JSON Walls and Floors into Hypar Elements.**

To use the sample JSON files in this folder:

1) Clone this repository or download one or more of the JSON files.
2) Login to [Hypar](https://hypar.io) and create a new Workflow.
3) After clicking the *Add Function* button, search for *JSON To Model*.
4) Click the *Insert* button on the *JSON To Model* function.
5) Open the function settings.
6) Drag + drop the downloaded JSON file into the File entry.
7) In the *Find* text box, enter *Walls*, *Floors*, or *Walls,Floors*.

To create your own Hypar JSON files from Revit 2020:

1) Clone this repository or download ExportWallsFloorsToHyparJSON.dyn
2) Use the sample RVT files in this folder or another Revit 2020 RVT containing Revit Walls, Floors, or both.
3) Open ExportWallsFloorsToHyparJSON.dyn in Dynamo.
4) Install the Hypar Dynamo package.
5) Run the Dynamo script.
6) In the same folder as the RVT, find the exported file called ExportedWallsFloors.json.
7) Follow steps 2 - 7 above.
