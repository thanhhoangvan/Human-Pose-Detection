<h1 align='center'>Human Pose Detection - Nhận dạng dáng người</h1>

<p align="center">
  <image src="cover.png" />
</p



# Train Dataset
[MPII Human Pose Dataset](http://human-pose.mpi-inf.mpg.de/)
- Khoảng 25k hình ảnh
- Hơn 40 nghìn người có các khớp cơ thể được dán nhãn
- Bao gồm 410 hoạt động của con người

> **Annotation description**
> - .annolist(imgidx) - annotations cho ảnh có `imgidx`
> 
> - .image.name - tên file ảnh
> - .annorect(ridx) - body annotations for a person ridx
>   - .x1, .y1, .x2, .y2 - coordinates of the head rectangle
>   - .scale - person scale w.r.t. 200 px height
>   - .objpos - rough human position in the image
>   - .annopoints.point - person-centric body joint annotations
>     - .x, .y - coordinates of a joint id - joint id (0 - r ankle, 1 - r knee, 2 - r hip, 3 - l hip, 4 - l knee, 5 - l ankle, 6 - pelvis, 7 - thorax, 8 - upper neck, 9 - head top, 10 - r wrist, 11 - r elbow, 12 - r shoulder, 13 - l shoulder, 14 - l elbow, 15 - l wrist)
>   - is_visible - joint visibility
>   - .vidx - Id của video trong danh sách video
>   - .frame_sec - Vị trí của ảnh trong video gốc, số giây
> - img_train(imgidx) - training/testing image assignment
> - single_person(imgidx) - contains rectangle id ridx of sufficiently separated individuals
> 
> - act(imgidx) - activity/category label for image imgidx
> 
> - act_name - activity name
>   - cat_name - category name
>   - act_id - activity id
> - video_list(videoidx) - specifies video id as is provided by YouTube. To watch video on youtube go to https://www.youtube.com/watch?v=video_list(videoidx)

# **Cài đặt môi trường - Enviroment**
- Python 3.8
- TensorFlow 2.8
- TensorRT 8.2 -> với `NVIDIA Jetson Nano`

