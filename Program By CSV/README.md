<img src="preview.png" width="512">
            

# Program By CSV

Converts a properly formatted Comma Separated Value (.csv, CSV) file into space program of [Room Definitions](https://raw.githubusercontent.com/hypar-io/Schemas/master/RoomDefinition.json) compatible with various Hypar space planning functions.

|Input Name|Type|Description|
|---|---|---|
|Program|Data|A CSV list of room definitions.|
|Use imperial units|Boolean|Default is metric units.|

The first row of the imported CSV file is assumed to be column headers and is ignored, but is included in this example to clarify the translation of each column entry to a corresponding property of the resulting Room Definitions:

| Suite Name | Suite Number | Department | Room Name | Room Quantity | Area | Room Ratio | Room Height |
|---|---|---|---|---|---|---|---|
| Classrooms | 1001 | Pedagogy | Event Space | 1 | 400 | 0.75 | 5.0 |

Other Hypar Functions can interpret each Room Definition in any way, but the format was designed with the following ideas in mind:

#### Suite Name | Suite Number
A pair of entries to uniquely designate a group of adjacent room types separated from each other by walls and accessed by horizontal circulation.

#### Department
Intended as an additional identifier for a group of rooms in case another functions can use the information.

#### Room Name
An identifier for a individual room type.

#### Room Quantity
The quantity of the rooms that will be derived from the Room Definition within the Suite.

#### Area
The square unit area for each room derived from the Room Definition.

#### Ratio
The dimensional ratio between the rectangular room sides.

#### Room Height
The height from the floor of this room type.

Program By CSV produces no geometry. The only outputs are statistics for the quantity of Room Definitions created in the current Hypar Model and their aggregate area if they were instantiated as individual rooms.

|Output Name|Type|Description|
|---|---|---|
|Room Definition Quantity|Number|The number of Room Definitions supplied to the model.|
|Aggregate Program Area|Number|Aggregate area of all Room Definitions.|

To use the CSV files in this folder:
1) Clone this repository or download one or more of the CSV files.
2) Login to hypar.io and create a new Workflow.
3) After clicking the *Add Function* button, search for *Program By CSV*.
4) Click the *Insert* button on the *Program By CSV* function.
5) Open the function settings.
6) Drag + drop the downloaded CSV file into the File entry.
7) Clicking the *Add Function* button again, search for *Plan By Program*.
8) Click the *Insert* button on the *Plan By Program* function.
