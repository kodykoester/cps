### Command Line Prompts and Scripts **[cps]**
Helpful command line [commands, prompts, scripts] I've used in the past. 



### Prompt for changing all file names in a directory from **Home Alone (1990)** to **home_alone_1990**

```bash
for f in *; do
    # Convert to lowercase, replace spaces with underscores, remove parentheses
    newname=$(echo "$f" | tr '[:upper:]' '[:lower:]' | tr ' ' '_' | tr -d '()')
    
    # Rename only if the new name is different
    if [ "$f" != "$newname" ]; then
        mv "$f" "$newname"
    fi
done
```

