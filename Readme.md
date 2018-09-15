# Granny Safe Auto 

Imagine if you would, a home so smart that it manifests a marriage of variegated sensors that consistently interact with the environment to implement a solution so secure that you would become the best of friends with the most grotesque of horror movies. Looks pleasant, doesn't it? We think so too. But like every marriage, its effectiveness is directly proportional to its simplicity. In other words, a system is only as effective and impactful as its ease and operability by its users. Therefore, using a grandma as our proverbial mascot, the aim of this project is to aggregate the wonders of modern technology and package it into a simple and robust system to empower the oldest section of our society.

We propose an adaptive, sustainable and secure IOT solution to enhance the lives of the elderly which focuses on making their lives as comfortable as one can imagine without burdening them with the hassles and sophistication of modern technology. We aim to bring the smartest of technologies to help safeguard people's homes, protect them from hazards and allay their fears from the dread of having to learn new tech. In our prototypic solution, we present a platform that monitors home security by integrating multiple IP cameras and detecting motion and people. We provide an alert based solution to detect threats, fraugery, natural calamities such as fire, earthquakes, etc. while ensuring ease of accessibilty and appropriate privacy.


# Usage 


---
1) Clone Repo

```
git clone https://github.com/rishunny/grannysafeauto.git
```

2) Pull Docker Image

```
docker pull bjoffe/openface_flask_v2
```

3) Run Docker image, make sure you mount your User (for MAC) or home (for Ubuntu) directory as a volume so you can access your local files

```
docker run -v "$(pwd)":/src -p 5000:5000 -t -i bjoffe/openface_flask_v2  /bin/bash
```

- Navigate to the home_surveillance project inside the volume within your Docker container
- Move into the system directory

```
cd system
```
4) Run WebApp.py
```
python WebApp.py
```
- Visit ```localhost:5000 ```
- Login Username: ```admin``` Password ```admin```

## Notes and Features ##

>### *Camera Settings*
- To add your own IP camera simply add the URL of the camera into field on the camera panel.

>### *Customizable Alerts*
- The Dashboard allows you to configure your own email and alarm trigger alerts. 
- The alerts panel allows you to set up certain events such as the recognition of a particular person or motion detection so that you receive an email alert when the event occurs. The confidence slider sets the accuracy that you would like to use for recognition events.

>### *Face Recognition and the Face Database*
- Faces that are detected are shown in the faces detected panel on the Dashboard.
- To perform accurate face recognition, twenty or more face images should be used. Furthermore, images taken in the surveillance environment (i.e. use the IP cameras to capture face images - this can be achieved by using the face_capture option in the SurveillanceSystem script and creating your own face directory) produce better results as a posed to adding images taken else where.
- A person is classified as unknown if they are recognised with a confidence lower than 20% or are predicted as unknown by the classifier.


## Ideas for Future developement ##

- Detecting fall of person

- Database Implementation

- Open set recognition for accurate identification of unknown people

- Behaviour recognition using neural networks

- Optimising motion detection and tracking algorithms

- Integration with third party services to recognise your friends and family

- The addition of home automation control features 

and many more...

# License
---

Copyright 2018, Rishu Agrawal, All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

- http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

# References
---

- Flask Web Server GPIO - http://mattrichardson.com/Raspberry-Pi-Flask/
- Openface Project - https://cmusatyalab.github.io/openface/
- Flask Websockets - http://blog.miguelgrinberg.com/post/easy-websockets-with-flask-and-gevent

 


 
