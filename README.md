# CXR_C19_DS
### Chest X-Ray Covid-19 Detection System 

[![CodeFactor](https://www.codefactor.io/repository/github/everlookneversee/cxr_c19_ds/badge)](https://www.codefactor.io/repository/github/everlookneversee/cxr_c19_ds)
![GitHub](https://img.shields.io/github/license/EverLookNeverSee/cxr_c19_ds)
![GitHub branch checks state](https://img.shields.io/github/checks-status/EverLookNeverSee/cxr_c19_ds/main)
![GitHub language count](https://img.shields.io/github/languages/count/EverLookNeverSee/cxr_c19_ds)
![GitHub top language](https://img.shields.io/github/languages/top/EverLookNeverSee/cxr_c19_ds)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/EverLookNeverSee/cxr_c19_ds)
![Lines of code](https://img.shields.io/tokei/lines/github/EverLookNeverSee/cxr_c19_ds)
![GitHub all releases](https://img.shields.io/github/downloads/EverLookNeverSee/cxr_c19_ds/total)
![GitHub issues](https://img.shields.io/github/issues-raw/EverLookNeverSee/cxr_c19_ds)
![GitHub pull requests](https://img.shields.io/github/issues-pr-raw/EverLookNeverSee/cxr_c19_ds)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/EverLookNeverSee/cxr_c19_ds)
![GitHub contributors](https://img.shields.io/github/contributors/EverLookNeverSee/cxr_c19_ds)
![GitHub last commit](https://img.shields.io/github/last-commit/EverLookNeverSee/cxr_c19_ds)


#### Pre-trained vgg-16 model architecture:
![Transferred model architecture](images/transferred_model.png)

## Description
Covid-19 detection system using chest x-ray images based on transfer learning. We used [VGG-16](https://keras.io/api/applications/vgg/#vgg16-function) pre-trained model
and fine-tuning to adapt model on our issue.

| Model name      | Accuracy  |  Epochs  |
| :---------      | :-------  |  :-----  |
| VGG-16          | %92       |  30      |

![Model Accuracy](images/Model%20Accuracy.png) ![Model Loss](images/Model%20Loss.png)

## Authors
* Milad Sadeghi DM [@EverLookNeverSee](https://github.com/EverLookNeverSee)

## Demo
Run command below to display arguments:
```shell
$ python3 demo.py --help

-m    --model          Path to saved model directory
-i    --image          Path to image file
-v    --verbose        Level of verbosity
```

Example:
```shell
$ python3 demo.py --verbose --model <path_to_saved_model_directory> --image <path_to_image_file>
```

## Training on your own dataset
Run command below to display arguments
```shell
$ python3 train.py --help

-d    --dataset             Path to dataset directory
-b    --batch-size          Batch size
-l    --learning-rate       Learning rate
-v    --verbose             Level of verbosity
-w    --workers             Number of workers(Hardware)
-e    --epochs              Number of epochs
-s    --save                Specify a directory path to save trained model
```

Example:
```shell
$ python3 train.py -d ~/dataset -b 32 -l 0.00001 -v -w 32 -e 100 -s ~/models/
```

## Useful links
* Dataset: [COVID-19 Radiography Database](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database)
* Trained model: [Download from google drive](https://drive.google.com/drive/folders/1oqrAVcaDbiHj37Eb6Juo7cigl5CP6P7R?usp=sharing)

## License
This project licensed under the **MIT License** - see the [LICENSE](LICENSE) file for more details.
