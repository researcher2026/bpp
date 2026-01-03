# LLM Evaluation Report
*Generated: 2025-08-26 11:40:03*

## Summary Statistics

| variant                        |   ('scaffolding_quality', 'mean') |   ('scaffolding_quality', 'std') |   ('scaffolding_quality', 'count') |   ('contextual_responsiveness', 'mean') |   ('contextual_responsiveness', 'std') |   ('contextual_responsiveness', 'count') |   ('helpfulness', 'mean') |   ('helpfulness', 'std') |   ('helpfulness', 'count') |   ('symbolic_strategy_use', 'mean') |   ('symbolic_strategy_use', 'std') |   ('symbolic_strategy_use', 'count') |   ('memory_conversation', 'mean') |   ('memory_conversation', 'std') |   ('memory_conversation', 'count') |
|:-------------------------------|----------------------------------:|---------------------------------:|-----------------------------------:|----------------------------------------:|---------------------------------------:|-----------------------------------------:|--------------------------:|-------------------------:|---------------------------:|------------------------------------:|-----------------------------------:|-------------------------------------:|----------------------------------:|---------------------------------:|-----------------------------------:|
| C0_full__global_warming        |                           3.33333 |                         0.994236 |                                 30 |                                 4.2     |                               0.924755 |                                       30 |                   4.46667 |                 0.571346 |                         30 |                             3.66667 |                           0.994236 |                                   30 |                           2.5     |                         1.45626  |                                 30 |
| C0_full__moon_phases           |                           3.72222 |                         0.701472 |                                 36 |                                 4.58333 |                               0.554205 |                                       36 |                   4.80556 |                 0.576663 |                         36 |                             4.08333 |                           0.937321 |                                   36 |                           3       |                         1.19523  |                                 36 |
| C1_no_memory__global_warming   |                           4       |                         0.58722  |                                 30 |                                 4.36667 |                               0.76489  |                                       30 |                   4.16667 |                 0.698932 |                         30 |                             3.63333 |                           0.964305 |                                   30 |                           3.36667 |                         0.964305 |                                 30 |
| C1_no_memory__moon_phases      |                           3.77778 |                         0.72155  |                                 36 |                                 3.97222 |                               0.774084 |                                       36 |                   4       |                 0.92582  |                         36 |                             3.47222 |                           1.10805  |                                   36 |                           2.91667 |                         0.840918 |                                 36 |
| C2_no_fuzzy__global_warming    |                           3.6     |                         0.723974 |                                 30 |                                 4.56667 |                               0.678911 |                                       30 |                   4.6     |                 0.621455 |                         30 |                             3.83333 |                           0.874281 |                                   30 |                           2.93333 |                         1.11211  |                                 30 |
| C2_no_fuzzy__moon_phases       |                           3.44444 |                         0.734631 |                                 36 |                                 4.33333 |                               0.676123 |                                       36 |                   4.58333 |                 0.603561 |                         36 |                             3.69444 |                           0.786291 |                                   36 |                           2.63889 |                         1.09942  |                                 36 |
| C3_no_boundary__global_warming |                           3.63333 |                         0.556053 |                                 30 |                                 4.53333 |                               0.62881  |                                       30 |                   4.6     |                 0.621455 |                         30 |                             3.9     |                           0.711967 |                                   30 |                           2.93333 |                         1.17248  |                                 30 |
| C3_no_boundary__moon_phases    |                           3.58333 |                         0.769972 |                                 36 |                                 4.33333 |                               0.676123 |                                       36 |                   4.52778 |                 0.506309 |                         36 |                             3.55556 |                           0.606839 |                                   36 |                           2.72222 |                         1.16155  |                                 36 |
| C4_vanilla__global_warming     |                           2.96667 |                         0.964305 |                                 30 |                                 4.1     |                               0.884736 |                                       30 |                   4.16667 |                 0.74664  |                         30 |                             3.16667 |                           1.01992  |                                   30 |                           2.13333 |                         1.10589  |                                 30 |
| C4_vanilla__moon_phases        |                           3.36111 |                         0.761682 |                                 36 |                                 4.47222 |                               0.559904 |                                       36 |                   4.36111 |                 0.723198 |                         36 |                             3.36111 |                           1.09942  |                                   36 |                           2.41667 |                         1.15573  |                                 36 |

---

## Metric: **Scaffolding Quality**
![scaffolding_quality](charts/scaffolding_quality_boxplot.png)

### ANOVA
- F = 4.345
- p = 0.00002

### Post-hoc: Tukey HSD (p < 0.05)
```
                        Multiple Comparison of Means - Tukey HSD, FWER=0.05                         
====================================================================================================
            group1                         group2             meandiff p-adj   lower   upper  reject
----------------------------------------------------------------------------------------------------
       C0_full__global_warming           C0_full__moon_phases   0.3889 0.5516 -0.2103  0.9881  False
       C0_full__global_warming   C1_no_memory__global_warming   0.6667 0.0264  0.0408  1.2925   True
       C0_full__global_warming      C1_no_memory__moon_phases   0.4444 0.3516 -0.1548  1.0436  False
       C0_full__global_warming    C2_no_fuzzy__global_warming   0.2667 0.9389 -0.3592  0.8925  False
       C0_full__global_warming       C2_no_fuzzy__moon_phases   0.1111 0.9999 -0.4881  0.7103  False
       C0_full__global_warming C3_no_boundary__global_warming      0.3 0.8804 -0.3258  0.9258  False
       C0_full__global_warming    C3_no_boundary__moon_phases     0.25 0.9462 -0.3492  0.8492  False
       C0_full__global_warming     C4_vanilla__global_warming  -0.3667 0.6915 -0.9925  0.2592  False
       C0_full__global_warming        C4_vanilla__moon_phases   0.0278    1.0 -0.5714   0.627  False
          C0_full__moon_phases   C1_no_memory__global_warming   0.2778 0.9004 -0.3214   0.877  False
          C0_full__moon_phases      C1_no_memory__moon_phases   0.0556    1.0 -0.5158  0.6269  False
          C0_full__moon_phases    C2_no_fuzzy__global_warming  -0.1222 0.9997 -0.7214   0.477  False
          C0_full__moon_phases       C2_no_fuzzy__moon_phases  -0.2778  0.871 -0.8491  0.2935  False
          C0_full__moon_phases C3_no_boundary__global_warming  -0.0889    1.0 -0.6881  0.5103  False
          C0_full__moon_phases    C3_no_boundary__moon_phases  -0.1389 0.9989 -0.7102  0.4324  False
          C0_full__moon_phases     C4_vanilla__global_warming  -0.7556 0.0029 -1.3548 -0.1564   True
          C0_full__moon_phases        C4_vanilla__moon_phases  -0.3611 0.5898 -0.9324  0.2102  False
  C1_no_memory__global_warming      C1_no_memory__moon_phases  -0.2222 0.9747 -0.8214   0.377  False
  C1_no_memory__global_warming    C2_no_fuzzy__global_warming     -0.4 0.5739 -1.0258  0.2258  False
  C1_no_memory__global_warming       C2_no_fuzzy__moon_phases  -0.5556 0.0954 -1.1548  0.0436  False
  C1_no_memory__global_warming C3_no_boundary__global_warming  -0.3667 0.6915 -0.9925  0.2592  False
  C1_no_memory__global_warming    C3_no_boundary__moon_phases  -0.4167 0.4482 -1.0159  0.1825  False
  C1_no_memory__global_warming     C4_vanilla__global_warming  -1.0333    0.0 -1.6592 -0.4075   True
  C1_no_memory__global_warming        C4_vanilla__moon_phases  -0.6389 0.0262 -1.2381 -0.0397   True
     C1_no_memory__moon_phases    C2_no_fuzzy__global_warming  -0.1778 0.9948  -0.777  0.4214  False
     C1_no_memory__moon_phases       C2_no_fuzzy__moon_phases  -0.3333 0.6966 -0.9046   0.238  False
     C1_no_memory__moon_phases C3_no_boundary__global_warming  -0.1444  0.999 -0.7436  0.4548  False
     C1_no_memory__moon_phases    C3_no_boundary__moon_phases  -0.1944 0.9859 -0.7658  0.3769  False
     C1_no_memory__moon_phases     C4_vanilla__global_warming  -0.8111 0.0009 -1.4103 -0.2119   True
     C1_no_memory__moon_phases        C4_vanilla__moon_phases  -0.4167 0.3765  -0.988  0.1546  False
   C2_no_fuzzy__global_warming       C2_no_fuzzy__moon_phases  -0.1556 0.9981 -0.7548  0.4436  False
   C2_no_fuzzy__global_warming C3_no_boundary__global_warming   0.0333    1.0 -0.5925  0.6592  False
   C2_no_fuzzy__global_warming    C3_no_boundary__moon_phases  -0.0167    1.0 -0.6159  0.5825  False
   C2_no_fuzzy__global_warming     C4_vanilla__global_warming  -0.6333 0.0447 -1.2592 -0.0075   True
   C2_no_fuzzy__global_warming        C4_vanilla__moon_phases  -0.2389 0.9595 -0.8381  0.3603  False
      C2_no_fuzzy__moon_phases C3_no_boundary__global_warming   0.1889 0.9919 -0.4103  0.7881  False
      C2_no_fuzzy__moon_phases    C3_no_boundary__moon_phases   0.1389 0.9989 -0.4324  0.7102  False
      C2_no_fuzzy__moon_phases     C4_vanilla__global_warming  -0.4778 0.2511  -1.077  0.1214  False
      C2_no_fuzzy__moon_phases        C4_vanilla__moon_phases  -0.0833    1.0 -0.6546   0.488  False
C3_no_boundary__global_warming    C3_no_boundary__moon_phases    -0.05    1.0 -0.6492  0.5492  False
C3_no_boundary__global_warming     C4_vanilla__global_warming  -0.6667 0.0264 -1.2925 -0.0408   True
C3_no_boundary__global_warming        C4_vanilla__moon_phases  -0.2722 0.9111 -0.8714   0.327  False
   C3_no_boundary__moon_phases     C4_vanilla__global_warming  -0.6167 0.0379 -1.2159 -0.0175   True
   C3_no_boundary__moon_phases        C4_vanilla__moon_phases  -0.2222 0.9654 -0.7935  0.3491  False
    C4_vanilla__global_warming        C4_vanilla__moon_phases   0.3944 0.5307 -0.2048  0.9936  False
----------------------------------------------------------------------------------------------------
```

---

## Metric: **Contextual Responsiveness**
![contextual_responsiveness](charts/contextual_responsiveness_boxplot.png)

### ANOVA
- F = 2.737
- p = 0.00432

### Post-hoc: Tukey HSD (p < 0.05)
```
                        Multiple Comparison of Means - Tukey HSD, FWER=0.05                         
====================================================================================================
            group1                         group2             meandiff p-adj   lower   upper  reject
----------------------------------------------------------------------------------------------------
       C0_full__global_warming           C0_full__moon_phases   0.3833 0.4824 -0.1805  0.9472  False
       C0_full__global_warming   C1_no_memory__global_warming   0.1667 0.9964 -0.4223  0.7556  False
       C0_full__global_warming      C1_no_memory__moon_phases  -0.2278  0.956 -0.7916  0.3361  False
       C0_full__global_warming    C2_no_fuzzy__global_warming   0.3667 0.6111 -0.2223  0.9556  False
       C0_full__global_warming       C2_no_fuzzy__moon_phases   0.1333 0.9991 -0.4305  0.6972  False
       C0_full__global_warming C3_no_boundary__global_warming   0.3333 0.7328 -0.2556  0.9223  False
       C0_full__global_warming    C3_no_boundary__moon_phases   0.1333 0.9991 -0.4305  0.6972  False
       C0_full__global_warming     C4_vanilla__global_warming     -0.1 0.9999 -0.6889  0.4889  False
       C0_full__global_warming        C4_vanilla__moon_phases   0.2722 0.8757 -0.2916  0.8361  False
          C0_full__moon_phases   C1_no_memory__global_warming  -0.2167 0.9681 -0.7805  0.3472  False
          C0_full__moon_phases      C1_no_memory__moon_phases  -0.6111 0.0124 -1.1487 -0.0735   True
          C0_full__moon_phases    C2_no_fuzzy__global_warming  -0.0167    1.0 -0.5805  0.5472  False
          C0_full__moon_phases       C2_no_fuzzy__moon_phases    -0.25 0.8987 -0.7876  0.2876  False
          C0_full__moon_phases C3_no_boundary__global_warming    -0.05    1.0 -0.6139  0.5139  False
          C0_full__moon_phases    C3_no_boundary__moon_phases    -0.25 0.8987 -0.7876  0.2876  False
          C0_full__moon_phases     C4_vanilla__global_warming  -0.4833 0.1658 -1.0472  0.0805  False
          C0_full__moon_phases        C4_vanilla__moon_phases  -0.1111 0.9997 -0.6487  0.4265  False
  C1_no_memory__global_warming      C1_no_memory__moon_phases  -0.3944 0.4392 -0.9583  0.1694  False
  C1_no_memory__global_warming    C2_no_fuzzy__global_warming      0.2 0.9862 -0.3889  0.7889  False
  C1_no_memory__global_warming       C2_no_fuzzy__moon_phases  -0.0333    1.0 -0.5972  0.5305  False
  C1_no_memory__global_warming C3_no_boundary__global_warming   0.1667 0.9964 -0.4223  0.7556  False
  C1_no_memory__global_warming    C3_no_boundary__moon_phases  -0.0333    1.0 -0.5972  0.5305  False
  C1_no_memory__global_warming     C4_vanilla__global_warming  -0.2667 0.9127 -0.8556  0.3223  False
  C1_no_memory__global_warming        C4_vanilla__moon_phases   0.1056 0.9999 -0.4583  0.6694  False
     C1_no_memory__moon_phases    C2_no_fuzzy__global_warming   0.5944 0.0296  0.0306  1.1583   True
     C1_no_memory__moon_phases       C2_no_fuzzy__moon_phases   0.3611 0.5006 -0.1765  0.8987  False
     C1_no_memory__moon_phases C3_no_boundary__global_warming   0.5611 0.0523 -0.0028   1.125  False
     C1_no_memory__moon_phases    C3_no_boundary__moon_phases   0.3611 0.5006 -0.1765  0.8987  False
     C1_no_memory__moon_phases     C4_vanilla__global_warming   0.1278 0.9994 -0.4361  0.6916  False
     C1_no_memory__moon_phases        C4_vanilla__moon_phases      0.5 0.0932 -0.0376  1.0376  False
   C2_no_fuzzy__global_warming       C2_no_fuzzy__moon_phases  -0.2333 0.9489 -0.7972  0.3305  False
   C2_no_fuzzy__global_warming C3_no_boundary__global_warming  -0.0333    1.0 -0.6223  0.5556  False
   C2_no_fuzzy__global_warming    C3_no_boundary__moon_phases  -0.2333 0.9489 -0.7972  0.3305  False
   C2_no_fuzzy__global_warming     C4_vanilla__global_warming  -0.4667 0.2593 -1.0556  0.1223  False
   C2_no_fuzzy__global_warming        C4_vanilla__moon_phases  -0.0944 0.9999 -0.6583  0.4694  False
      C2_no_fuzzy__moon_phases C3_no_boundary__global_warming      0.2 0.9813 -0.3639  0.7639  False
      C2_no_fuzzy__moon_phases    C3_no_boundary__moon_phases      0.0    1.0 -0.5376  0.5376  False
      C2_no_fuzzy__moon_phases     C4_vanilla__global_warming  -0.2333 0.9489 -0.7972  0.3305  False
      C2_no_fuzzy__moon_phases        C4_vanilla__moon_phases   0.1389 0.9982 -0.3987  0.6765  False
C3_no_boundary__global_warming    C3_no_boundary__moon_phases     -0.2 0.9813 -0.7639  0.3639  False
C3_no_boundary__global_warming     C4_vanilla__global_warming  -0.4333 0.3635 -1.0223  0.1556  False
C3_no_boundary__global_warming        C4_vanilla__moon_phases  -0.0611    1.0  -0.625  0.5028  False
   C3_no_boundary__moon_phases     C4_vanilla__global_warming  -0.2333 0.9489 -0.7972  0.3305  False
   C3_no_boundary__moon_phases        C4_vanilla__moon_phases   0.1389 0.9982 -0.3987  0.6765  False
    C4_vanilla__global_warming        C4_vanilla__moon_phases   0.3722 0.5265 -0.1916  0.9361  False
----------------------------------------------------------------------------------------------------
```

---

## Metric: **Helpfulness**
![helpfulness](charts/helpfulness_boxplot.png)

### ANOVA
- F = 4.703
- p = 0.00001

### Post-hoc: Tukey HSD (p < 0.05)
```
                        Multiple Comparison of Means - Tukey HSD, FWER=0.05                         
====================================================================================================
            group1                         group2             meandiff p-adj   lower   upper  reject
----------------------------------------------------------------------------------------------------
       C0_full__global_warming           C0_full__moon_phases   0.3389 0.5682 -0.1892   0.867  False
       C0_full__global_warming   C1_no_memory__global_warming     -0.3 0.7759 -0.8516  0.2516  False
       C0_full__global_warming      C1_no_memory__moon_phases  -0.4667 0.1357 -0.9948  0.0615  False
       C0_full__global_warming    C2_no_fuzzy__global_warming   0.1333 0.9989 -0.4183  0.6849  False
       C0_full__global_warming       C2_no_fuzzy__moon_phases   0.1167 0.9995 -0.4115  0.6448  False
       C0_full__global_warming C3_no_boundary__global_warming   0.1333 0.9989 -0.4183  0.6849  False
       C0_full__global_warming    C3_no_boundary__moon_phases   0.0611    1.0  -0.467  0.5892  False
       C0_full__global_warming     C4_vanilla__global_warming     -0.3 0.7759 -0.8516  0.2516  False
       C0_full__global_warming        C4_vanilla__moon_phases  -0.1056 0.9998 -0.6337  0.4226  False
          C0_full__moon_phases   C1_no_memory__global_warming  -0.6389 0.0054  -1.167 -0.1108   True
          C0_full__moon_phases      C1_no_memory__moon_phases  -0.8056    0.0 -1.3091  -0.302   True
          C0_full__moon_phases    C2_no_fuzzy__global_warming  -0.2056 0.9653 -0.7337  0.3226  False
          C0_full__moon_phases       C2_no_fuzzy__moon_phases  -0.2222 0.9248 -0.7258  0.2813  False
          C0_full__moon_phases C3_no_boundary__global_warming  -0.2056 0.9653 -0.7337  0.3226  False
          C0_full__moon_phases    C3_no_boundary__moon_phases  -0.2778 0.7611 -0.7813  0.2258  False
          C0_full__moon_phases     C4_vanilla__global_warming  -0.6389 0.0054  -1.167 -0.1108   True
          C0_full__moon_phases        C4_vanilla__moon_phases  -0.4444 0.1367  -0.948  0.0591  False
  C1_no_memory__global_warming      C1_no_memory__moon_phases  -0.1667 0.9918 -0.6948  0.3615  False
  C1_no_memory__global_warming    C2_no_fuzzy__global_warming   0.4333 0.2708 -0.1183  0.9849  False
  C1_no_memory__global_warming       C2_no_fuzzy__moon_phases   0.4167 0.2651 -0.1115  0.9448  False
  C1_no_memory__global_warming C3_no_boundary__global_warming   0.4333 0.2708 -0.1183  0.9849  False
  C1_no_memory__global_warming    C3_no_boundary__moon_phases   0.3611 0.4737  -0.167  0.8892  False
  C1_no_memory__global_warming     C4_vanilla__global_warming      0.0    1.0 -0.5516  0.5516  False
  C1_no_memory__global_warming        C4_vanilla__moon_phases   0.1944 0.9759 -0.3337  0.7226  False
     C1_no_memory__moon_phases    C2_no_fuzzy__global_warming      0.6 0.0125  0.0719  1.1281   True
     C1_no_memory__moon_phases       C2_no_fuzzy__moon_phases   0.5833 0.0097  0.0798  1.0869   True
     C1_no_memory__moon_phases C3_no_boundary__global_warming      0.6 0.0125  0.0719  1.1281   True
     C1_no_memory__moon_phases    C3_no_boundary__moon_phases   0.5278 0.0314  0.0242  1.0313   True
     C1_no_memory__moon_phases     C4_vanilla__global_warming   0.1667 0.9918 -0.3615  0.6948  False
     C1_no_memory__moon_phases        C4_vanilla__moon_phases   0.3611 0.4017 -0.1424  0.8647  False
   C2_no_fuzzy__global_warming       C2_no_fuzzy__moon_phases  -0.0167    1.0 -0.5448  0.5115  False
   C2_no_fuzzy__global_warming C3_no_boundary__global_warming      0.0    1.0 -0.5516  0.5516  False
   C2_no_fuzzy__global_warming    C3_no_boundary__moon_phases  -0.0722    1.0 -0.6004  0.4559  False
   C2_no_fuzzy__global_warming     C4_vanilla__global_warming  -0.4333 0.2708 -0.9849  0.1183  False
   C2_no_fuzzy__global_warming        C4_vanilla__moon_phases  -0.2389 0.9132  -0.767  0.2892  False
      C2_no_fuzzy__moon_phases C3_no_boundary__global_warming   0.0167    1.0 -0.5115  0.5448  False
      C2_no_fuzzy__moon_phases    C3_no_boundary__moon_phases  -0.0556    1.0 -0.5591   0.448  False
      C2_no_fuzzy__moon_phases     C4_vanilla__global_warming  -0.4167 0.2651 -0.9448  0.1115  False
      C2_no_fuzzy__moon_phases        C4_vanilla__moon_phases  -0.2222 0.9248 -0.7258  0.2813  False
C3_no_boundary__global_warming    C3_no_boundary__moon_phases  -0.0722    1.0 -0.6004  0.4559  False
C3_no_boundary__global_warming     C4_vanilla__global_warming  -0.4333 0.2708 -0.9849  0.1183  False
C3_no_boundary__global_warming        C4_vanilla__moon_phases  -0.2389 0.9132  -0.767  0.2892  False
   C3_no_boundary__moon_phases     C4_vanilla__global_warming  -0.3611 0.4737 -0.8892   0.167  False
   C3_no_boundary__moon_phases        C4_vanilla__moon_phases  -0.1667 0.9885 -0.6702  0.3369  False
    C4_vanilla__global_warming        C4_vanilla__moon_phases   0.1944 0.9759 -0.3337  0.7226  False
----------------------------------------------------------------------------------------------------
```

---

## Metric: **Symbolic Strategy Use**
![symbolic_strategy_use](charts/symbolic_strategy_use_boxplot.png)

### ANOVA
- F = 2.751
- p = 0.00413

### Post-hoc: Tukey HSD (p < 0.05)
```
                        Multiple Comparison of Means - Tukey HSD, FWER=0.05                         
====================================================================================================
            group1                         group2             meandiff p-adj   lower   upper  reject
----------------------------------------------------------------------------------------------------
       C0_full__global_warming           C0_full__moon_phases   0.4167 0.7195 -0.3111  1.1445  False
       C0_full__global_warming   C1_no_memory__global_warming  -0.0333    1.0 -0.7935  0.7268  False
       C0_full__global_warming      C1_no_memory__moon_phases  -0.1944 0.9977 -0.9223  0.5334  False
       C0_full__global_warming    C2_no_fuzzy__global_warming   0.1667 0.9995 -0.5935  0.9268  False
       C0_full__global_warming       C2_no_fuzzy__moon_phases   0.0278    1.0    -0.7  0.7556  False
       C0_full__global_warming C3_no_boundary__global_warming   0.2333 0.9933 -0.5268  0.9935  False
       C0_full__global_warming    C3_no_boundary__moon_phases  -0.1111    1.0 -0.8389  0.6167  False
       C0_full__global_warming     C4_vanilla__global_warming     -0.5 0.5319 -1.2602  0.2602  False
       C0_full__global_warming        C4_vanilla__moon_phases  -0.3056 0.9441 -1.0334  0.4223  False
          C0_full__moon_phases   C1_no_memory__global_warming    -0.45 0.6207 -1.1778  0.2778  False
          C0_full__moon_phases      C1_no_memory__moon_phases  -0.6111 0.1389 -1.3051  0.0828  False
          C0_full__moon_phases    C2_no_fuzzy__global_warming    -0.25  0.985 -0.9778  0.4778  False
          C0_full__moon_phases       C2_no_fuzzy__moon_phases  -0.3889 0.7439 -1.0828  0.3051  False
          C0_full__moon_phases C3_no_boundary__global_warming  -0.1833 0.9985 -0.9111  0.5445  False
          C0_full__moon_phases    C3_no_boundary__moon_phases  -0.5278 0.3155 -1.2217  0.1662  False
          C0_full__moon_phases     C4_vanilla__global_warming  -0.9167  0.003 -1.6445 -0.1889   True
          C0_full__moon_phases        C4_vanilla__moon_phases  -0.7222 0.0338 -1.4162 -0.0283   True
  C1_no_memory__global_warming      C1_no_memory__moon_phases  -0.1611 0.9995 -0.8889  0.5667  False
  C1_no_memory__global_warming    C2_no_fuzzy__global_warming      0.2 0.9979 -0.5602  0.9602  False
  C1_no_memory__global_warming       C2_no_fuzzy__moon_phases   0.0611    1.0 -0.6667  0.7889  False
  C1_no_memory__global_warming C3_no_boundary__global_warming   0.2667 0.9827 -0.4935  1.0268  False
  C1_no_memory__global_warming    C3_no_boundary__moon_phases  -0.0778    1.0 -0.8056    0.65  False
  C1_no_memory__global_warming     C4_vanilla__global_warming  -0.4667 0.6305 -1.2268  0.2935  False
  C1_no_memory__global_warming        C4_vanilla__moon_phases  -0.2722 0.9732    -1.0  0.4556  False
     C1_no_memory__moon_phases    C2_no_fuzzy__global_warming   0.3611 0.8566 -0.3667  1.0889  False
     C1_no_memory__moon_phases       C2_no_fuzzy__moon_phases   0.2222 0.9909 -0.4717  0.9162  False
     C1_no_memory__moon_phases C3_no_boundary__global_warming   0.4278 0.6875    -0.3  1.1556  False
     C1_no_memory__moon_phases    C3_no_boundary__moon_phases   0.0833    1.0 -0.6106  0.7773  False
     C1_no_memory__moon_phases     C4_vanilla__global_warming  -0.3056 0.9441 -1.0334  0.4223  False
     C1_no_memory__moon_phases        C4_vanilla__moon_phases  -0.1111    1.0 -0.8051  0.5828  False
   C2_no_fuzzy__global_warming       C2_no_fuzzy__moon_phases  -0.1389 0.9998 -0.8667  0.5889  False
   C2_no_fuzzy__global_warming C3_no_boundary__global_warming   0.0667    1.0 -0.6935  0.8268  False
   C2_no_fuzzy__global_warming    C3_no_boundary__moon_phases  -0.2778 0.9694 -1.0056    0.45  False
   C2_no_fuzzy__global_warming     C4_vanilla__global_warming  -0.6667 0.1428 -1.4268  0.0935  False
   C2_no_fuzzy__global_warming        C4_vanilla__moon_phases  -0.4722  0.552    -1.2  0.2556  False
      C2_no_fuzzy__moon_phases C3_no_boundary__global_warming   0.2056 0.9964 -0.5223  0.9334  False
      C2_no_fuzzy__moon_phases    C3_no_boundary__moon_phases  -0.1389 0.9998 -0.8328  0.5551  False
      C2_no_fuzzy__moon_phases     C4_vanilla__global_warming  -0.5278 0.3851 -1.2556     0.2  False
      C2_no_fuzzy__moon_phases        C4_vanilla__moon_phases  -0.3333  0.879 -1.0273  0.3606  False
C3_no_boundary__global_warming    C3_no_boundary__moon_phases  -0.3444 0.8884 -1.0723  0.3834  False
C3_no_boundary__global_warming     C4_vanilla__global_warming  -0.7333  0.069 -1.4935  0.0268  False
C3_no_boundary__global_warming        C4_vanilla__moon_phases  -0.5389 0.3542 -1.2667  0.1889  False
   C3_no_boundary__moon_phases     C4_vanilla__global_warming  -0.3889 0.7935 -1.1167  0.3389  False
   C3_no_boundary__moon_phases        C4_vanilla__moon_phases  -0.1944 0.9966 -0.8884  0.4995  False
    C4_vanilla__global_warming        C4_vanilla__moon_phases   0.1944 0.9977 -0.5334  0.9223  False
----------------------------------------------------------------------------------------------------
```

---

## Metric: **Memory Conversation**
![memory_conversation](charts/memory_conversation_boxplot.png)

### ANOVA
- F = 2.980
- p = 0.00202

### Post-hoc: Tukey HSD (p < 0.05)
```
                        Multiple Comparison of Means - Tukey HSD, FWER=0.05                         
====================================================================================================
            group1                         group2             meandiff p-adj   lower   upper  reject
----------------------------------------------------------------------------------------------------
       C0_full__global_warming           C0_full__moon_phases      0.5 0.7441 -0.3923  1.3923  False
       C0_full__global_warming   C1_no_memory__global_warming   0.8667 0.0933 -0.0653  1.7987  False
       C0_full__global_warming      C1_no_memory__moon_phases   0.4167 0.8963 -0.4757   1.309  False
       C0_full__global_warming    C2_no_fuzzy__global_warming   0.4333 0.8987 -0.4987  1.3653  False
       C0_full__global_warming       C2_no_fuzzy__moon_phases   0.1389    1.0 -0.7534  1.0312  False
       C0_full__global_warming C3_no_boundary__global_warming   0.4333 0.8987 -0.4987  1.3653  False
       C0_full__global_warming    C3_no_boundary__moon_phases   0.2222 0.9986 -0.6701  1.1145  False
       C0_full__global_warming     C4_vanilla__global_warming  -0.3667 0.9628 -1.2987  0.5653  False
       C0_full__global_warming        C4_vanilla__moon_phases  -0.0833    1.0 -0.9757   0.809  False
          C0_full__moon_phases   C1_no_memory__global_warming   0.3667  0.951 -0.5257   1.259  False
          C0_full__moon_phases      C1_no_memory__moon_phases  -0.0833    1.0 -0.9341  0.7675  False
          C0_full__moon_phases    C2_no_fuzzy__global_warming  -0.0667    1.0  -0.959  0.8257  False
          C0_full__moon_phases       C2_no_fuzzy__moon_phases  -0.3611 0.9403 -1.2119  0.4897  False
          C0_full__moon_phases C3_no_boundary__global_warming  -0.0667    1.0  -0.959  0.8257  False
          C0_full__moon_phases    C3_no_boundary__moon_phases  -0.2778 0.9895 -1.1286   0.573  False
          C0_full__moon_phases     C4_vanilla__global_warming  -0.8667 0.0651  -1.759  0.0257  False
          C0_full__moon_phases        C4_vanilla__moon_phases  -0.5833 0.4696 -1.4341  0.2675  False
  C1_no_memory__global_warming      C1_no_memory__moon_phases    -0.45 0.8442 -1.3423  0.4423  False
  C1_no_memory__global_warming    C2_no_fuzzy__global_warming  -0.4333 0.8987 -1.3653  0.4987  False
  C1_no_memory__global_warming       C2_no_fuzzy__moon_phases  -0.7278 0.2225 -1.6201  0.1645  False
  C1_no_memory__global_warming C3_no_boundary__global_warming  -0.4333 0.8987 -1.3653  0.4987  False
  C1_no_memory__global_warming    C3_no_boundary__moon_phases  -0.6444 0.3911 -1.5368  0.2479  False
  C1_no_memory__global_warming     C4_vanilla__global_warming  -1.2333 0.0013 -2.1653 -0.3013   True
  C1_no_memory__global_warming        C4_vanilla__moon_phases    -0.95 0.0266 -1.8423 -0.0577   True
     C1_no_memory__moon_phases    C2_no_fuzzy__global_warming   0.0167    1.0 -0.8757   0.909  False
     C1_no_memory__moon_phases       C2_no_fuzzy__moon_phases  -0.2778 0.9895 -1.1286   0.573  False
     C1_no_memory__moon_phases C3_no_boundary__global_warming   0.0167    1.0 -0.8757   0.909  False
     C1_no_memory__moon_phases    C3_no_boundary__moon_phases  -0.1944 0.9993 -1.0452  0.6563  False
     C1_no_memory__moon_phases     C4_vanilla__global_warming  -0.7833 0.1419 -1.6757   0.109  False
     C1_no_memory__moon_phases        C4_vanilla__moon_phases     -0.5 0.6877 -1.3508  0.3508  False
   C2_no_fuzzy__global_warming       C2_no_fuzzy__moon_phases  -0.2944 0.9887 -1.1868  0.5979  False
   C2_no_fuzzy__global_warming C3_no_boundary__global_warming      0.0    1.0  -0.932   0.932  False
   C2_no_fuzzy__global_warming    C3_no_boundary__moon_phases  -0.2111 0.9991 -1.1034  0.6812  False
   C2_no_fuzzy__global_warming     C4_vanilla__global_warming     -0.8 0.1643  -1.732   0.132  False
   C2_no_fuzzy__global_warming        C4_vanilla__moon_phases  -0.5167  0.706  -1.409  0.3757  False
      C2_no_fuzzy__moon_phases C3_no_boundary__global_warming   0.2944 0.9887 -0.5979  1.1868  False
      C2_no_fuzzy__moon_phases    C3_no_boundary__moon_phases   0.0833    1.0 -0.7675  0.9341  False
      C2_no_fuzzy__moon_phases     C4_vanilla__global_warming  -0.5056 0.7316 -1.3979  0.3868  False
      C2_no_fuzzy__moon_phases        C4_vanilla__moon_phases  -0.2222  0.998  -1.073  0.6286  False
C3_no_boundary__global_warming    C3_no_boundary__moon_phases  -0.2111 0.9991 -1.1034  0.6812  False
C3_no_boundary__global_warming     C4_vanilla__global_warming     -0.8 0.1643  -1.732   0.132  False
C3_no_boundary__global_warming        C4_vanilla__moon_phases  -0.5167  0.706  -1.409  0.3757  False
   C3_no_boundary__moon_phases     C4_vanilla__global_warming  -0.5889 0.5269 -1.4812  0.3034  False
   C3_no_boundary__moon_phases        C4_vanilla__moon_phases  -0.3056 0.9796 -1.1563  0.5452  False
    C4_vanilla__global_warming        C4_vanilla__moon_phases   0.2833 0.9914  -0.609  1.1757  False
----------------------------------------------------------------------------------------------------
```

