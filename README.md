# robust3DPose

This is a github repository for robust3DPose.

## Qualitative Results

<p align="center"><img src="images/indian_dance.gif" width="100%" alt="" >

## Quantitative Results
Our method is evaluated on [Human3.6M](http://vision.imar.ro/human3.6m/description.php) and [Humaneva](http://humaneva.is.tue.mpg.de/).

Evaluation metric consists of ```MPJPE(mean per-joint position error)``` and ```P-MPJPE(Procrustes-aligned MPJPE)```.

To evaluate our method, we conducted six types of data, including **five occlusions(random box, moving box, fixed box lower/middle/upper)**.

For example, ```moving box``` in Human3.6M is shown below:
<p align="center"><img src="images/h36m_moving_box.gif" width="100%" alt="" /></p>

### Human3.6M


#### VideoPose3D
| Data Type | VideoPose3D | Our method + VideoPose3D |
|:-------|:-------:|:-------:|
| Normal | 57.7 / 44.0 | 54.3 / 41.8 |
| Random Box | 90.2 / 67.0 | 70.5 / 53.2 |
| Moving Box | 111.1 / 79.7 | 65.3 / 50.4 |
| Fixed Box Lower | 107.9 / 85.6 | 72.4 / 55.4 |
| Fixed Box Middle | 220.9 / 145.5 | 78.4 / 59.2  |
| Fixed Box Upper | 311.0 / 216.8 | 90.0 / 69.6 |

#### MixSTE
| Data Type | MixSTE | Our method + MixSTE |
|:-------|:-------:|:-------:|
| Normal | 66.6 / 51.2 | 44.0 / 36.3 |
| Random Box | 128.5 / 102.4 | 66.1 / 51.6 |
| Moving Box | 100.3 / 79.5 | 63.7 / 51.1 |
| Fixed Box Lower | 99.8 / 83.4 | 64.8 / 52.5 |
| Fixed Box Middle | 141.8 / 115.0 | 76.8 / 59.8 |
| Fixed Box Upper | 172.7 / 134.2 | 87.5 / 69.0 |

#### MHFormer
| Data Type | MHFormer | Our method + MHFormer |
|:-------|:-------:|:-------:|
| Normal | 69.2 / 51.4 | 53.2 / 41.4 |
| Random Box | 123.9 / 96.1 | 165.9 / 104.0 |
| Moving Box | 99.3 / 74.8 | 125.6 / 83.8 |
| Fixed Box Lower | 103.7 / 82.2 | 97.7 / 68.8 |
| Fixed Box Middle | 138.6 / 111.5 | 200.2 / 111.6 |
| Fixed Box Upper | 166.7 / 126.4 | 168.7 / 110.1 |

#### P-STMO
| Data Type | P-STMO | Our method + P-STMO |
|:-------|:-------:|:-------:|
| Normal | 64.9 / 50.3 | 54.8 / 42.7 |
| Random Box | 174.2 / 110.4 | 125.8 / 77.5 |
| Moving Box | 133.9 / 96.3 | 89.7 / 63.0 |
| Fixed Box Lower | 147.9 / 106.7 | 93.3 / 65.4 |
| Fixed Box Middle | 162.2 / 110.8 | 100.7 / 70.7 |
| Fixed Box Upper | 371.8 / 288.2 | 157.9 / 100.0 |

#### MeTRAbs
| Data Type | MeTRAbs |
|:-------|:-------:|
| Normal | 48.6 / 36.8 |
| Random Box | 154.6 / 107.6 |
| Moving Box | 109.1 / 76.1 |
| Fixed Box Lower | 99.6 / 69.3 |
| Fixed Box Middle | 143.3 / 100.3 |
| Fixed Box Upper | 197.2 / 139.8 |

### Humaneva
We select only **four joints (left elbow, left knee, right elbow, right knee)** in Humaneva evaluation because we used models pretrained on Human3.6M and there are some errors from discrepancy between training dataset(Human3.6M) and evaluation dataset(Humaneva). 

#### VideoPose3D
| Data Type | VideoPose3D | Our method + VideoPose3D |
|:-------|:-------:|:-------:|
| Normal | 61.5 / 37.8 | 62.2 / 38.0 |
| Random Box | 80.1 / 51.8 | 70.6 / 45.5 |
| Moving Box | 63.8 / 40.7 | 63.6 / 39.5 |
| Fixed Box Lower | 93.0 / 60.9 | 66.1 / 43.3 |
| Fixed Box Middle | 313.8 / 165.2 | 72.4 / 47.1 |
| Fixed Box Upper | 192.9 / 144.6 | 151.4 / 94.0 |

#### MixSTE
| Data Type | MixSTE | Our method + MixSTE |
|:-------|:-------:|:-------:|
| Normal | 75.4 / 45.5 | 59.1 / 38.4 |
| Random Box | 134.2 / 74.8 | 69.9 / 46.0 |
| Moving Box | 74.6 / 49.1 | 61.2 / 40.5 |
| Fixed Box Lower | 88.9 / 60.1 | 62.7 / 43.4 |
| Fixed Box Middle | 180.2 / 92.1 | 91.2 / 57.2 |
| Fixed Box Upper | 132.5 / 81.7 | 124.8 / 69.5 |

#### MHFormer
| Data Type | MHFormer | Our method + MHFormer |
|:-------|:-------:|:-------:|
| Normal | 81.0 / 53.2 | 57.7 / 38.2 |
| Random Box | 128.6 / 70.4 | 119.5 / 44.5 |
| Moving Box | 82.5 / 55.5 | 59.9 / 40.0 |
| Fixed Box Lower | 103.8 / 69.7 | 72.5 / 44.5 |
| Fixed Box Middle | 172.8 / 88.5 | 173.1 / 73.6 |
| Fixed Box Upper | 134.2 / 79.6 | 185.2 / 50.6 |

#### P-STMO
| Data Type | P-STMO | Our method + P-STMO |
|:-------|:-------:|:-------:|
| Normal | 93.4 / 44.5 | 92.6 / 42.5 |
| Random Box | 157.0 / 72.9 | 127.4 / 54.9 |
| Moving Box | 94.3 / 46.8 | 93.5 / 44.0 |
| Fixed Box Lower | 119.4 / 66.1 | 100.5 / 47.2 |
| Fixed Box Middle | 159.6 / 67.9 | 121.9 / 54.4 |
| Fixed Box Upper | 201.2 / 96.3 | 166.6 / 69.7 |

#### MeTRAbs
| Data Type | MeTRAbs |
|:-------|:-------:|
| Normal | 54.2 / 37.4 |
| Random Box | 64.8 / 43.9 |
| Moving Box | 57.9 / 40.0 |
| Fixed Box Lower | 59.8 / 42.3 |
| Fixed Box Middle | 77.0 / 49.3 |
| Fixed Box Upper | 94.0 / 54.7 |