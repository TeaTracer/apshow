# Description
Visualization of site->subsite->appversion graph in various colors based on membership in subsets.

It will have several visualization modes.

First one is [JQ](https://github.com/stedolan/jq)-llke mode.
Output is a colored JSON opened in terminal using paginator.
It also could be redirected to output file.

Other possible modes:
* PNG-image with infographics
* Excel-table
* Human-readable text


# Usage
It's a binary CLI tool. Use it in your terminal.
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

# Roadmap

1. Write SQL for --query
2. Write simple Go program that could parse SQL output (PostgerSQL\`s psql tool) and print it
3. Handle <init graph file> and <appversion subset file> flags and print them to console
4. Use color to highlight <init graph file>\`s appversions contained in <appversion subset file>
5. Add algorithm which is able to hide branches of single color
6. Standartize the output in order to have an opportunity to compare different outputs
7. Add pagination to JQ-like mode
8. Prepare MVP: add documentation and examples
  
# Ideas

1. Use default location of <init graph file> like ~/.apshow and get rid of first positional argument
2. Use a mode for working with database directly (for those who have an access)
