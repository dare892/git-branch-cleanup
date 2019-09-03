# Git Branch Cleanup
A quick bash script to clean up remote and local branches.

##### First make cleanup.sh file
```
#!/bin/bash
array=(
  placeholder-branch1
  placeholder-brach2
)
for i in "${array[@]}"
do
  echo "DELETING $i"
  git branch -D $i
  git push origin --delete $i
done
```

##### In the array section, get rid of placeholders and replace it with your branches on the repo. In order to view your branches, do 
```
$ git branch
```

##### After you save, change permissions
```
chmod +x cleanup.sh
```

##### Run the script
```
using ./cleanup.sh
```
