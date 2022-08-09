# Abstract

<html>
<style>
    .abstract_table {
        border-top-style: hidden;
        border-bottom-style: hidden;
        border-left-style: hidden;
        border-right-style: hidden;
        }
    p {
        text-align:justify;
    }
</style>
<table class="abstract_table">
    <tr style="height:auto;">
        <td style="width:30%;">
            <!-- <img src="./img/abstract.png" > -->
            <!-- <embed src="./img/abstract.svg"  > -->
            <img src="./img/abstract.svg">
        </td>
        <td style="width:70%;text-align:justify">
            <font size=5><b>TIVE</b></font> is a Toolbox for Identifying Video instacne segmentation Errors. By directly operating output prediction files, TIVE can isolate error predictions and weight each type’s demage to mAP, in purpose of distinguishing model charactors. By decomposing localization quality in spatial-temporal dimensions, model’s potential drawbacks on spatial segmentation and temporal association can be clearly revealed. TIVE can also report mAP over instance temporal length for real applications. <a href="https://arxiv.org/abs/1911.12451">UAP</a> and <a href="https://dbolya.github.io/tide/">TIDE</a> are the formerly introduced error analyzing tools for image-level object recognition.

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
<html>
<style type="text/css">
.model_summary_table  {border:none;border-collapse:collapse;border-color:#93a1a1;border-spacing:0;}
.model_summary_table td{background-color:#fdf6e3;border-color:#93a1a1;border-style:solid;border-width:0px;color:#002b36;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.model_summary_table th{background-color:#657b83;border-color:#93a1a1;border-style:solid;border-width:0px;color:#fdf6e3;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.model_summary_table .model_summary_table-b406{background-color:#eee8d5;border-color:inherit;text-align:center;vertical-align:middle}
.model_summary_table .model_summary_table-9wq8{border-color:inherit;text-align:center;vertical-align:middle}
.model_summary_table .model_summary_table-ezbu{background-color:#eee8d5;border-color:inherit;text-align:center;vertical-align:top}
.model_summary_table .model_summary_table-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.model_summary_table .model_summary_table-hxaf{background-color:#657b83;border-color:#93a1a1;color:#fdf6e3;text-align:center;vertical-align:middle}
</style>
<table class="model_summary_table">
<thead>
  <tr>
    <th class="model_summary_table-9wq8" rowspan="2">Method</th>
    <th class="model_summary_table-9wq8" rowspan="2">Pretrain</th>
    <th class="model_summary_table-9wq8" rowspan="2">Training<br>Frames</th>
    <th class="model_summary_table-9wq8" colspan="4">Metrics </th>
    <th class="model_summary_table-9wq8" colspan="7">Error Weights(&amp;DeltaAP@50)</th>
  </tr>
  <tr>
    <th class="model_summary_table-hxaf">mAP</th>
    <th class="model_summary_table-hxaf">mAPs</th>
    <th class="model_summary_table-hxaf">mAPm</th>
    <th class="model_summary_table-hxaf">mAPl</th>
    <th class="model_summary_table-hxaf">Cls</th>
    <th class="model_summary_table-hxaf">Dup</th>
    <th class="model_summary_table-hxaf">Spat</th>
    <th class="model_summary_table-hxaf">Temp</th>
    <th class="model_summary_table-hxaf">Both</th>
    <th class="model_summary_table-hxaf">Bkg</th>
    <th class="model_summary_table-hxaf">Miss</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="model_summary_table-9wq8">Mask Track R-CNN</td>
    <td class="model_summary_table-9wq8">MSCOCO</td>
    <td class="model_summary_table-9wq8">T=2</td>
    <td class="model_summary_table-9wq8">36.30</td>
    <td class="model_summary_table-9wq8">10.44</td>
    <td class="model_summary_table-9wq8">35.87</td>
    <td class="model_summary_table-9wq8">43.43</td>
    <td class="model_summary_table-9wq8">7.50</td>
    <td class="model_summary_table-9wq8">0.00</td>
    <td class="model_summary_table-9wq8">6.73</td>
    <td class="model_summary_table-9wq8">6.30</td>
    <td class="model_summary_table-9wq8">0.24</td>
    <td class="model_summary_table-9wq8">0.94</td>
    <td class="model_summary_table-9wq8">6.08</td>
  </tr>
  <tr>
    <td class="model_summary_table-b406">VISOLO</td>
    <td class="model_summary_table-b406">MSCOCO</td>
    <td class="model_summary_table-b406">T=3</td>
    <td class="model_summary_table-b406">38.00</td>
    <td class="model_summary_table-b406">8.82</td>
    <td class="model_summary_table-b406">39.43</td>
    <td class="model_summary_table-b406">37.96</td>
    <td class="model_summary_table-b406">11.52</td>
    <td class="model_summary_table-b406">0.00</td>
    <td class="model_summary_table-b406">3.53</td>
    <td class="model_summary_table-b406">9.97</td>
    <td class="model_summary_table-b406">0.15</td>
    <td class="model_summary_table-b406">1.17</td>
    <td class="model_summary_table-b406">6.00</td>
  </tr>
  <tr>
    <td class="model_summary_table-9wq8">IFC</td>
    <td class="model_summary_table-9wq8">MSCOCO</td>
    <td class="model_summary_table-9wq8">T=5</td>
    <td class="model_summary_table-9wq8">40.35</td>
    <td class="model_summary_table-9wq8">21.05</td>
    <td class="model_summary_table-9wq8">39.04</td>
    <td class="model_summary_table-9wq8">41.09</td>
    <td class="model_summary_table-9wq8">6.81</td>
    <td class="model_summary_table-9wq8">0.02</td>
    <td class="model_summary_table-9wq8">8.55</td>
    <td class="model_summary_table-9wq8">9.46</td>
    <td class="model_summary_table-9wq8">0.41</td>
    <td class="model_summary_table-9wq8">1.13</td>
    <td class="model_summary_table-9wq8">4.68</td>
  </tr>
  <tr>
    <td class="model_summary_table-b406">SeqFormer</td>
    <td class="model_summary_table-ezbu">MSCOCO</td>
    <td class="model_summary_table-ezbu">T=5</td>
    <td class="model_summary_table-b406">43.37</td>
    <td class="model_summary_table-b406">21.69</td>
    <td class="model_summary_table-b406">40.43</td>
    <td class="model_summary_table-b406">39.20</td>
    <td class="model_summary_table-b406">6.95</td>
    <td class="model_summary_table-b406">0.25</td>
    <td class="model_summary_table-b406">6.99</td>
    <td class="model_summary_table-b406">4.47</td>
    <td class="model_summary_table-b406">0.00</td>
    <td class="model_summary_table-b406">0.97</td>
    <td class="model_summary_table-b406">6.20</td>
  </tr>
  <tr>
    <td class="model_summary_table-9wq8">Mask2Former</td>
    <td class="model_summary_table-c3ow">MSCOCO</td>
    <td class="model_summary_table-c3ow">T=2</td>
    <td class="model_summary_table-9wq8">48.20</td>
    <td class="model_summary_table-9wq8">26.37</td>
    <td class="model_summary_table-9wq8">44.10</td>
    <td class="model_summary_table-9wq8">45.19</td>
    <td class="model_summary_table-9wq8">4.15</td>
    <td class="model_summary_table-9wq8">0.15</td>
    <td class="model_summary_table-9wq8">4.89</td>
    <td class="model_summary_table-9wq8">7.21</td>
    <td class="model_summary_table-9wq8">0.19</td>
    <td class="model_summary_table-9wq8">2.03</td>
    <td class="model_summary_table-9wq8">3.19</td>
  </tr>
</tbody>
</table>
</html>

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
