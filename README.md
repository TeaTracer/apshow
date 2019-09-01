# Description
Visualization of site->subsite->appversion graph in various colors based on membership in subsets.

# Usage
***
```
apshow --query
```
Print the SQL which should be used to set the initial appversion configuration.
***
```
apshow <init graph file>
```
Print the full appversion\`s graph using the file with the output of --query\`s SQL.
***
```
apshow <init graph file> <appversion subset file>
```
Print the appversion\`s graph paited with two colors. Branches are joined based on colors.
