# squad-study
squad-study

## Docker Setting
```
docker run -it --rm -v $(realpath .):/src pytorch/pytorch:1.1.0-cuda10.0-cudnn7.5-devel
```

## How to Submit

```
cl upload [SOURCE FILE/DIRECTORY PATH(LOCAL)] -n [BUNDLE NAME(FOR CODALAB)]
cl run [PATH(FOR PARAMETER)]:[UUID(IN CODALAB)] "python [PATH(FOR PARAMETER)]/run_squad.py [PATH(FOR PARAMETER)]"
	--request-memory [WANTED]g --request-gpus 1 -n [BUNDLE NAME(FOR CODALAB)] --request-docker-image [DOCKERHUB PATH]
cl macro squad-utils/dev-evaluate-v1.1 [PREDICTIONS FILE UUID]
```

[example]
```
cl make run-predictions:0xa1b2c3d4/predictions.json -n predictions-YIYC //Is a directory error
cl make 0xa1b2c3d4e5w6q7t9z1x2d3s5w4q8w9e5w1s1/predictions.json -n
cl make run-predictions/predictions.json -n predictions-YIYC //Use last bundle

cl macro squad-utils/dev-evaluate-v1.1 predictions-YIYC
```


## Readings

* Submission tutorial https://worksheets.codalab.org/worksheets/0x8403d867f9a3444685c344f4f0bc8d34
* Codalab Run Tutorial https://github.com/graykode/KorQuAD-beginner/blob/master/README.md

## CodaLab Worksheets Link

* lee2102k@gmail.com https://worksheets.codalab.org/worksheets/0x2bae7809fc6947fa815dc6f83ccc57ad/
