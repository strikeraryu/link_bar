# LINK_BAR
Easy to use Terminal-based profile level bookmarking for URLs for developers `(Tested for mac)`

## Setup
1. Download `.link_bar.sh` (Use Below Command)
```
curl -LJO https://raw.githubusercontent.com/strikeraryu/link_bar/master/.link_bar.sh
```
2. Add `source <folder_path>/.link_bar.sh` to your zshrc file (Use Below Command)
```
echo "\nsource $PWD/.link_bar.sh" >> ~/.zshrc
```


## Usage

### lbadd
To add new alias for a link, with a optional field to set detault profile <br>
Command - `lbadd <alaias> <link> [optional] <profile>` <br>
Eg. 
```
lbadd google https://www.google.com/
``` 
```
lbadd google https://www.google.com/ "Profile 1"
```

### lbls
To show all alias, use flag -l to get detailed view with links <br>
Command - `lbls [optional] -l` <br>
Eg. 
```
lbls
```
```
meet 
google 
meet2 
```
#### Using flag `-l`
```
lbadd -l
```
```
meet https://meet.new/ Profile 1
google https://www.google.com/ 
meet2 https://meet.new/ Profile 2
```

### lbopen
To open a alias, in a specifc profile <br>
Command - `lbopen [optional] <profile>` <br>
Eg. 
```
lbopen meet
```
```
lbopen meet "Profile 2"
```
Order of precedence for profile `argument passed(in lbopen) > alias default profile(set in lbadd) > global default`

## ENV VARIABELS
- `LINK_BAR_PATH` - Path of the link file
- `LB_DEFAULT_PROFILE` - Global default profile

### Note
Profile are named as `"Default", "Profile 1", "Profile 2".....`
