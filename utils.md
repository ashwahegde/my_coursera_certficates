# Maintaining the repository

## Creating combined directory

```bash
find "." -name '*.pdf' -not -path "./exclude_this_directory/*" -exec cp {} combined/ \;
```

-   this copies all **pdf** files in current directory (recursively traverses sub-directories)
-   ignores exclude_this_directory.
-   copies it to [`combined`](/combined) directory.

## Creating Tree structure in [README.md](/README.md)

```bash
go run go/parser.go ~/myrepos/coursera_certficates/ "-" 4 combined
```

here:
-   it traverses through above directory.
-   uses `-` for points.
-   adds 4 spaces for indentation.
-   go/parser.go is available in different repository.
