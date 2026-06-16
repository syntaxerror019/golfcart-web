+++
date = '2025-08-11T12:00:15+08:00'
draft = false
title = 'Driving with AI'
categories = 'Ford Think Neighbor'
tags =['ai']
series = 'headline'
[params]
    author = 'Miles Hilliard & Jonas Wirz'
    thumbnail = 'https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/train_batch0.jpg'
    headline = ''
+++

We are experimenting with a few different approaches to autonomous driving on the Ford Think Neighbor, including YOLO (Computer Vision), SLAM (Simultaneous Localization and Mapping (LiDAR)), and GPS.

<!--more-->

To begin with, we took a look at YOLO to see if we could train a custom model to detect important objects around the vehicle. We drove the car around our school campus and collected over 2,000 photos of the car's surroundings. We were sure to include various lighting and environmental conditions in our dataset which would permit a more robust and functional model in the end. The only downside was the fact that we had to “teach” the AI what it would be looking for. This meant that we had to go through and manually label every object in every photo. This was a time consuming process, but we were eventually able to come up with a dataset that we were proud of.

To do this, we divided our dataset into chunks and gave them to different people in the shop to do hand labeling. After a few weeks of pretty consistent work, this step was done and it became time to train our custom AI for the first time.

We then used this annotated dataset to train a custom YOLOv11 model to detect the following objects:

- People
- Other Vehicles
- Traffic Signs
- Pedestrian Crossings

![YOLOv11 TRAINING](https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/train_batch0.jpg)

Once we hand labeled and finished training our model, we tested its accuracy. After much tweaking, we were able to achieve an mAP@0.5 of 64% and an mAP@0.5:0.95 of 39%. Not too bad, but clearly not good enough to safely drive the car autonomously by itself.

Once we had the AI trained, we upgraded the camera to be safer and have better quality. We mounted a camera housing to the top of the golf cart which provides the camera inside protection from the rain and other weather events. 

Driving around with the AI running seemed to yield some promising results...

![Camera on the roof](https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/Camerainstall.webp)

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
            src="https://www.youtube.com/embed/wncYFLaLN_4" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
    </iframe>
</div>

{{< gallery >}}
https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/YOLO1.webp
https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/YOLO2.png
https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/2.webp
https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/4.webp
https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/Cameratube.webp
https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/YOLOModelCamera/CameraHolder1.webp
{{< /gallery >}}