# Make single tag
## 0.1m tag 8"x8"
`./make_calib_board.py --type apriltag --nx 1 --ny 1 --tsize 0.1 --tspace 0 --marginx 0.0513 --marginy 0.0513 --color Black --borderbits 2 --startid 120`


## 0.2m tag 12"x12"
`./make_calib_board.py --type apriltag --nx 1 --ny 1 --tsize 0.2 --tspace 0 --marginx 0.052 --marginy 0.052 --color Black --borderbits 2 --startid 123`


## 0.3m tag - 16"x16"
`./make_calib_board.py --type apriltag --nx 1 --ny 1 --tsize 0.3 --tspace 0 --marginx 0.0528 --marginy 0.0528 --color Black --borderbits 2 --startid 120`

## 0.4m tag - 20"x20"
`./make_calib_board.py --type apriltag --nx 1 --ny 1 --tsize 0.4 --tspace 0 --marginx 0.0536 --marginy 0.0536 --color Black --borderbits 2 --startid 126`

# Examine them:

`pdfinfo target.pdf`

(device pts by 72 to get inches!)

# How to make the tags for cage 2:

`./make_apriltags.py --type apriltag --nx 9 --ny 8 --tsize 0.04 --tspace 0.2`

# How to make a large calibration target

front side: 5x7 april grid with 34" x 46"

`./make_calib_board.py --type apriltag --nx 5 --ny 7 --tsize 0.125 --tspace 0.25 --marginx 0.02519715 --marginy 0.0213465833333 ; pdfinfo target.pdf`

back side:

`./make_calib_board.py --type checkerboard --nx 5 --ny 7 --csx 0.14 --csy 0.14 --marginx 0.011447639 --marginy 0.0238478; pdfinfo target.pdf`

# How to make the aviary tag boards (20x16)

```
for ((s=0;s<108;s+=6))
do
./make_calib_board.py --type apriltag --nx 3 --ny 2 --tsize 0.12 --tspace 0.25 --marginx 0.01364721 --marginy 0.03784723472222222222 --color Violet --startid $s --borderbits 1
mv target.pdf target_$s.pdf
done
```

# How to make a FLA canvas tag

`./make_calib_board.py --type apriltag --nx 1 --ny 1 --tsize 1.25 --tspace 0 --marginx 0.162 --marginy 0.25 --color Black --startid 100`


