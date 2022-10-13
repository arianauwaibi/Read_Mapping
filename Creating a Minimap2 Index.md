# Creating a Minimap2 Index 

[Access to Minimap2 Manual](https://lh3.github.io/minimap2/minimap2.html#4)

  Their [GitHub Page](https://github.com/lh3/minimap2)

Index with 1 strain

```
minimap2 -d BS13-02_strains.mmi BS13-02.fna
```

# Creating an index with Multiple strains

```
minimap2 -d strains.mmi [ BS13-02.fna W11_06.fna ]
```

Did not work 

```
minimap2 -d strains_folder.mmi /home/jovyan/Strains
```

Did not work
