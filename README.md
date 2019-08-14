# squad-study
squad-study

## Docker Setting
```
docker run -it --rm -v $(realpath .):/src pytorch/pytorch:1.1.0-cuda10.0-cudnn7.5-devel
```

## How to Submit

[example]
```
cl make run-predictions:0xa1b2c3d4/predictions.json -n predictions-YIYC //Is a directory error
cl make 0xa1b2c3d4e5w6q7t9z1x2d3s5w4q8w9e5w1s1/predictions.json -n
cl make run-predictions/predictions.json -n predictions-YIYC //Use last bundle

cl macro squad-utils/dev-evaluate-v1.1 predictions-YIYC
```


## Readings

* Submission tutorial https://worksheets.codalab.org/worksheets/0x8403d867f9a3444685c344f4f0bc8d34
