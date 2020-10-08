# Simulator/Mock Server to generate Fixed Format 
This python projects creates mock data in fixed file format.

In order to do that, it needs one configuration file which is in source code.

## Technologies Used
Python 3.x

## Pre-requisute
Faker library must be installed. If it is not present, run as below:
```
pip install Faker
```
## Configuring input file
Sample configuration file is as below:
```
{
    #Number of Rows to be generated
    "number-of-rows": 1000,
    # Name, will be used for output file name
    "name": "fixed-file-demo",
    # absolute path for output directory
    "output-file-absolute-path": "c:/tmp",
    # Length of each record, as its fixed format file. It is addition of all width column mentioned below
    "per-record-length": 84,
    "properties": [
        {
            #Position of element in output file, order is important
            "position": 1,
            #Name of column
            "column-name": "Recodrd Id",
            #size/width of column
            "width": 6,
            #what kind of data to be generated, supported type as of now are number, date, enum, string, filler
            "data-type": "number"
        },
        {
            "position": 2,
            "column-name": "Recording Date",
            "width": 8,
            "data-type": "date"
        },
        {
            "position": 3,
            "column-name": "Orginating Number",
            "width": 10,
            "data-type": "number"
        },
        {
            "position": 4,
            "column-name": "Service Code",
            "width": 3,
            "data-type": "enum",
            "enum-values" : ["823", "777"]
        },
        {
            "position": 5,
            "column-name": "RPC",
            "width": 3,
            "data-type": "number"
        },
        {
            "position": 6,
            "column-name": "Name",
            "width": 23,
            "data-type": "string"
        },
        {
            "position": 7,
            "column-name": "FILLER",
            "width": 5,
            "data-type": "filler"
        },
        {
            "position": 8,
            "column-name": "Incoming Conversion Rate",
            "width": 6,
            "data-type": "number"
        },
        {
            "position": 9,
            "column-name": "ERROR CODE",
            "width": 3,
            "data-type": "filler"
        },
        {
            "position": 10,
            "column-name": "TRX",
            "width": 10,
            "data-type": "filler"
        },
        {
            "position": 11,
            "column-name": "START TIME hhmmsst",
            "width": 7,
            "data-type": "time"
        }
        
    ]
}
```
## How to Execute Simulator
### 1. Using jupyter (anaconda/ google colab / Visual Studio code - Jupyter association)
1. [Google Colab](https://colab.research.google.com/#create=true)
2. [Anaconda](https://www.anaconda.com/products/individual)
   
   i. Install Faker using `pip install Faker`

   ii. Open `simulator-jupyter.ipynb` file into notebook.

   iii. Run the notebook

   ```
   **Please note, if you are executing on google colab, uncomment the lines to print the output on screen. By default, google colab will not have access to your local system.**

   It is advised to run it on Visual Studio code or Anaconda Jupyter.
   ```

### 2. Using python file to execute
     i. Install Faker using `pip install Faker`
 
     ii. Open `FixedFileFormatMockGenerator.py` file in any editor preferable Visual Studio Code, pycharm editor.

     iii. Run the program

## Output
Output would looks like below:
```
Reading input config file...
Number of rows to be generated: 1000
Output will be written to c:/tmp/fixed-file-demo.dat
Starting with mock data generation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
Finshed with mock data generation*******************
Time taken for execution to generate 1000 of the program is 0.31467151641845703
```


