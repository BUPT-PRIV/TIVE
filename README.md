# Abstract

<html>
<style>
    table,tr,td {
        border-top-style: hidden;
        border-bottom-style: hidden;
        border-left-style: hidden;
        border-right-style: hidden;
        }
    p {
        text-align:justify;
    }
</style>
<table >
    <tr style="height:auto;">
        <td style="width:30%;">
            <!-- <img src="./img/abstract.png" > -->
            <!-- <embed src="./img/abstract.svg"  > -->
            <img src="./img/abstract.svg">
        </td>
        <td style="width:70%;text-align:justify">
            <font size=5><b>TIVE</b></font> is a Toolbox for Identifying Video instacne segmentation Errors. By directly operating output prediction files, TIVE can isolate error predictions and weight each type’s demage to mAP, in purpose of distinguishing model charactors. By decomposing localization quality in spatial-temporal dimensions, model’s potential drawbacks on spatial segmentation and temporal association can be clearly revealed. TIVE can also report mAP over instance temporal length for real applications. [UAP](https://arxiv.org/abs/1911.12451) and [TIDE](https://dbolya.github.io/tide/) are the formerly introduced error analyzing tools for image-level object recognition.

We expect that the analysis of TIVE can give the researchers more insights, guiding the community to promote more meaningful explorations for video instance segmentation.

</td>
</tr>
</table>
</html>

# Error Types
<div align=center>
    <img src="./img/ErrorType.svg">
</div>
<p>
    <font size=5><b>TIVE </b></font>bin false positives and false negatives produced by a model into 7 types, including general object recognition errors and two spatial-temporal localization errors with specific focus on spatial segmentation and temporal association quality of predicted mask sequence.
</p>

# Error identification
<div align=center>
    <img src="./img/Error_identification.svg">
</div>
<p>
    Clear pictures are given to show errors produced by models cross all temporal length, effect of each to the evaluation metric is weighted by individually fixing oracle. Users can observe what prevents their model to achieve higher mAP.
</p>

# Model Summary
Experiments conducted by TIVE show that recognizing short video instances is especially challenging, mAP corss temporal ranges and error distributions for all models selected by our paper are shown below.

############# chart ###############


# Citation

If you use TIVE in your project, please cite

```
@inproceedings{jia2022tive,
  author    = {Wenhe Jia and Lu Yang and Zilong Jia and Wenyi Zhao and Qing Song},
  title     = {TIVE: A General Toolbox for Identifying Video Instance Segemntation Errors},
  booktitle = {arXiv},
  year      = {2022},
}
```
