# Linux Commands

## cat

### Echo files contents:
```
cat [-n] [-s] FILE_NAME, [FILE_NAME, ...]
```

**-n**: Echo line numbers. (Optional)  
**-s**: Skip empty lines

### Create/Edit file:
```
cat >FILE_NAME
```
`ENTER`
```
CONTENT
```

### Copy file content to another one: 
```
cat ORIGIN > DESTINATION
```
*Overides existing content

### Append file content to another one:
```
cat ORIGIN >> DESITION
```

## clear
Clear the terminal: `clear`.

## Copy file contents
```
pbcopy < [FILE_NAME]
```