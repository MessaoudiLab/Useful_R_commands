## Reading in a file
```
objectname <- read.delim("filename.xls", sep="\t", header=TRUE)
```

## Writing a file
```
write.table(objectname, file="filename.xls", sep="\t", quote=FALSE, col.names=TRUE, row.names=FALSE)
```
NOTE if there are row names just change the argument to TRUE.

## Merging 2 dataframes
Usually to merge dataframes of the same dimensions based on a common column
```
objectname <- merge(object1, object2, by.x="NameofCommonColumn_in_object1", by.y="NameofCommonColumn_in_object2", all=TRUE)
```

## Subsetting a dataframe to include or exclude columns
To include:
```
objectname <- subset(object_to_be_subsetted, select=c(columnA, columnB, columnC))
```

To exclude:
```
objectname <- subset(object_to_be_subsetted, select= -c(columnA, columnB, columnC))
```

## Subsetting a dataframe based on a list
```
object <- [dataframe[dataframe[,#]%in%list,]
```

NOTE: "#" refers to the column number that shares the same values contained in the list
