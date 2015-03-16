# Useful Tips #
## Maya Tips ##
### catch ###
This example shows how catch can be used to handle failure of commands or procedures.  This will catch errors and calls to procedures that do not exist.

```
catch ( `underConstruction` );
```

Without the catch, if the execution of underConstruction failed at runtime, the whole script containing the call would fail. Using catch enables this script to continue execution even if something fails.

### match ###
To make sure the current object isn't an attribute, or a component.

```
string $sel[] = `ls -sl`;
for( $a in $sel )
    if( `match "[.\[]+" $a` == "" )
        print "It's an object.";
```

## Windows Tips ##
### start ###
To open a file with the default program assigned.

```
start "" "H:\LIBRERIA\caspa\ApacheTommySeebach.avi"
```