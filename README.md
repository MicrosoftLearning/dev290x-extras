# dev290x-extras

## 1. Zip the entire CocoMS folder
`zip -r CocoMS.zip CocoMS`

> We can't upload CocoMS.zip to GitHub for the following reasons:
![](./assets/limit.png)

## 2. Create a folder to hold the split zip files

`mkdir CocoMS-zipsplit`

## 3. Split the single zip file into 25MB files


`zipsplit -b ./CocoMS-zipsplit/ -n 26214400 CocoMS.zip`


## 4. Upload to destination

## 5. Concatenate split zips

`cat CocoMS*.zip > CocoMS-whole.zip`

## 6. re-build index of zip file

`zip -FF CocoMS-whole.zip --out CocoMS.zip`

## 7. Unzip to destination

`unzip CocoMS.zip


