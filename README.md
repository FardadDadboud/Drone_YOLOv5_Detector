The <a href="https://github.com/ultralytics/yolov5.git" target="_blank">YOLOv5</a> model has been trained with combination of WOSDETC Drone-Vs-Bird detection competition and Det-Fly datasets in September 2021.

YOLOv5 is a family of object detection architectures and models pretrained on the COCO dataset, and represents Ultralytics open-source research into future vision AI methods, incorporating lessons learned and best practices evolved over thousands of hours of research and development.

See the [YOLOv5 Docs](https://docs.ultralytics.com) for full documentation on training, testing and deployment.

Install:
Python>=3.6.0 is required with all requirements.txt installed including PyTorch>=1.7:

$ cd yolov5
$ pip install -r requirements.txt

Inference with detect.py:

`detect.py` runs inference on a variety of sources and saving results to `runs/detect`.

$ python detect.py --source 0  # webcam

                            img.jpg  # image
                            vid.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
                            
$ python detect.py --weight ./best.pt --source 'path/to/the/video' --augment --save-txt --save-conf --device=0,1,2,3 --img 1280




    --source', type=str, default=ROOT / 'data/images', help='file/dir/URL/glob, 0 for webcam'
    --imgsz', '--img', '--img-size', nargs='+', type=int, default=[640], help='inference size h,w'
    --device', default='', help='cuda device, i.e. 0 or 0,1,2,3 or cpu'
    --save-txt', action='store_true', help='save results to *.txt'
    --save-conf', action='store_true', help='save confidences in --save-txt labels'
    --save-crop', action='store_true', help='save cropped prediction boxes'
    --classes', nargs='+', type=int, help='filter by class: --classes 0, or --classes 0 2 3'
    --augment', action='store_true', help='augmented inference'\
    --project', default=ROOT / 'runs/detect', help='save results to project/name'
    --name', default='exp', help='save results to project/name'


Please fork/download the <a href="https://github.com/ultralytics/yolov5.git" target="_blank">YOLOv5</a> or this repository and then download the weight from <a href="https://drive.google.com/file/d/1hNgnhu47S8TIyVxfhOAe72YLDccKjw4d/view?usp=sharing" target="_blank">here</a> and put it anywhere you want. You should change "--weight ./best.pt" parameter of detect.py module to anywhere that you put the weight.
