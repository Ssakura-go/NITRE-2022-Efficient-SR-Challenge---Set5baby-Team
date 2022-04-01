## [NTIRE 2022 Workshop and Challenge](https://data.vision.ee.ethz.ch/cvl/ntire22/) @ CVPR 2022


## Details of the backage [Set5babyteam]
The backage named [Set5babyteam] includes code file as well as the usage in [Set5babyteam / statement.txt] and pdf as well as sub-enclosure of  .tex source files of factsheet in [Set5babyteam /factsheet/ Set5babyteam-factsheet.zip].

Additionally, our model is trained with EDSR structure, please check it is running with the right range of inputs. And we will note the change in the [Set5babyteam / change.txt].

## Efficient Super-Resolution Challenge


Jointly with NTIRE workshop we have a challenge on Efficient Super-Resolution, that is, the task of super-resolving (increasing the resolution) an input image with a magnification factor x4 based on a set of prior examples of low and corresponding high resolution images. The challenge has three tracks.

**[Track 1: Parameters](https://competitions.codalab.org/competitions/20167)**, the aim is to obtain a network design / solution with the lowest amount of parameters while being constrained to maintain or improve the PSNR result and the inference time (runtime) of IMDN ([Hui et al, 2017](https://arxiv.org/abs/1909.11856)).

**[Track 2: Inference](https://competitions.codalab.org/competitions/20168)**, the aim is to obtain a network design / solution with the lowest inference time (runtime) on a common GPU (ie. Titan Xp) while being constrained to maintain or improve over IMDN ([Hui et al, 2017](https://arxiv.org/abs/1909.11856)) in terms of number of parameters and the PSNR result.

**[Track 3: Fidelity](https://competitions.codalab.org/competitions/20169)**, the aim is to obtain a network design / solution with the best fidelity (PSNR) while being constrained to maintain or improve over IMDN ([Hui et al, 2017](https://arxiv.org/abs/1909.11856)) in terms of number of parameters and inference time on a common GPU (ie. Titan Xp).

## Baseline model (IMDN)

* Number of parameters: 893,936 (0.89M)

    ```python
    number_parameters = sum(map(lambda x: x.numel(), model.parameters()))
    ```

* Average PSNR on validation data: 29.13 dB

* Average inference time (Titan Xp) on validation data: 0.10 second 

    Note: The best average inference time among three trials is selected.

Run [test_demo.py](test_demo.py) to test the model

## How to use the code during test phase.

1. `https://github.com/Ssakura-go/NITRE-2022-Efficient-SR-Challenge---Set5baby-Team.git`
2. `python test_demo.py`
