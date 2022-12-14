# Report-of-Animal-Detection-Project
This is a report of an Animal Detection Project I did summer of 2020. 

CS animal AI project

By: Mihir Konda date:11/23/2020

Help from Piyush Kumar

**Purpose and start for the project:**

I've always been interested in computer science and when I started classes with Mr. Kumar initially taught me python3 however, before Covid he introduced me to AI. More specifically, an image recognition software and an introduction to neural networks. During Covid I was introduced to YOLOv3, a new image recognition software that I was interested in. I wanted to create something that was able to detect animals in my backyard and potentially send a message to me along the lines of "be careful there is a snake in your yard." I quickly realized this ambition was not possible so I wanted to use YOLOv3 to create a software that would be able to detect different animals. I initially spent a large amount of my time researching AI, neural networks and how exactly image recognition works. I had to learn how linux and VM's work.

**How does AI work and where is it used?:**

Artificial Intelligence (AI) is a system of intelligent algorithms, neural networks and machine learning to essentially mimic tasks that typically require human intelligence to automation. In short, AI allows humans to save time in tasks such as responding to emails. Essentially, AI uses machine learning and historical data to create an accurate model or prediction of the coming events. For example, chess is a game that is completely dominated by computers in modern times however, it wasn't always like this. Before 1997, computers in chess were based purely algorithms and sometimes took significant time to calculate moves. However, Deep Blue used AI and machine learning to beat Garry Kasparov, world champion, in 1997. Deep Blue and modern chess computers use past games to analyze patterns and then calculate the best moves based on probabilities. M In our case, image recognition is a part of AI in which a computer is able to analyze different metadata and structure such as color, pixel length, given tags and opacity to name a few. Image recognition is used in e-commerce, automobile industry and can assist in medical imagery. A common starting point for building up an AI system is using a neural network.

Neural networks are unique in the way they are able to break down a complex question into a system of yes or no questions and then change these into binary that computers can understand. Each dot in a neural network is breaking down a complex question with a different idea. For example, lets say a basic problem is "Should I go outside today?" using 3 questions "Do I have to wear a jacket today?", "Is the forecast saying it will be nice today", and "Does the weather look nice today." Each of these questions has a weight; perhaps the forecast is more important than whether you have a jacket on making the weights 2 and 1.5 respectively. Each question has a 0 or 1 answer and multiplied times the weights will allow for a complex question to be deduced down to a single number. Having layers of these neural networks allows for computers to make decisions based on previous and changing data. Perhaps the weather tends to be worse than the forecast potentially tweaking the weight to what reflects more on previous data. After making a system with layers of neural networks it should be able to reproduce 1 number relating to the big question (most of the time probability of said event occurring)

**Methodology and YOLO implementation:**

YOLOv3, stands for You Only Look Once, is one of the newest real time object detectors and it has one of the shortest inference times of all current detectors. Inference time is essentially the time it takes for the program to make a prediction. It is extremely fast and accurate. YOLO applies a different approach than traditional detection systems. ![](RackMultipart20220925-1-c6zooj_html_7e797c7e3ec68b64.png)

![image](https://user-images.githubusercontent.com/84816566/192124042-4fcc6966-b955-4f67-a694-ed51c914a9b3.png)


Image courtesy of [https://pjreddie.com/darknet/yolo/](https://pjreddie.com/darknet/yolo/) shows the significantly faster inference time of YOLOv3 compared to modern image recognition software.

"We apply a single neural network to the full image. This network divides the image into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the predicted probabilities." (from YOLO website). YOLOv3 needs a linux operating system since my native OS is windows I had to install a ubuntu virtual machine. This was through an application called Virtual Box. Virtual machines essentially allow you to use some of your PC's ram to emulate a different OS. Next, I had to install the git clone from the YOLOv3 site and darknet as well. Darknet is an open source neural network framework that contains YOLOv3 on it. From here we are able to access and use the default image recognition that YOLOv3 provides such objects like dogs, bicycles, trucks and airplanes among others are detectable with this. However, different animal detection is my goal and the default didn't include some animals like snakes, alligators, rabbits, bears and such. Using a Training YOLOv3 github where I was able to train the AI with hundreds of images of the given animals. Once I had all my requirements I needed to download hundreds of images from Google and tag them. I used a microsoft product called VoTT (Visual Object Tagging Tool) . It allowed me to efficiently manually tag hundreds of images; this process is very arduous because I had to constantly delete certain images that weren't relevant or had other animals in the background. Then after I was able to use Windows power shell to run my script and it worked with about 82.2% confidence and with the exact speices being rpedicated at a 73% rate.

**Conclusion:**

Ultimately, I learned a significant amount from this project from trial and error. I learned how to: troubleshoot, apply github, image tag and run a virtual machine. Along with this I struggled with many complications before coming to a solution to the problem. Initially, I tried Cygwin which is a Unix-like environment that allows for command-line interface for Windows. My mistake is that I thought it was exactly like a virtual environment however, certain packages like csv export which is needed for running VoTT through my images. There was no way around this problem as natively that package was able to run on Cygwin; meaning I had to restart my project however, this failure showed me the importance of checking modules/package limitations and to truly understand the application I'm using. I made other mistakes like not tagging properly and editing folder order, these failures culminate to improve my final product. This project was an amazing experience and helped me understand more about computer science.

**Works Cited**

1. Redmon, Joseph. _YOLO: Real-Time Object Detection_, [pjreddie.com/darknet/yolo/](https://pjreddie.com/darknet/yolo/)
2. "Artificial Intelligence ??? What It Is and Why It Matters." _SAS_, [www.sas.com/en\_us/insights/analytics/what-is-artificial-intelligence.html](http://www.sas.com/en_us/insights/analytics/what-is-artificial-intelligence.html)
3. "How Does AI Work?" _YouTube_, YouTube, 23 Apr. 2017, [www.youtube.com/watch?v=L\_9OluD0nqw](http://www.youtube.com/watch?v=L_9OluD0nqw)
4. HubSpot. "What Is Artificial Intelligence (or Machine Learning)?" _YouTube_, YouTube, 30 Jan. 2017, [www.youtube.com/watch?v=mJeNghZXtMo](http://www.youtube.com/watch?v=mJeNghZXtMo)
5. "Welcome to VirtualBox.org!" _Oracle VM VirtualBox_, [www.virtualbox.org/](http://www.virtualbox.org/)
6. "What Is a Virtual Machine and How Does It Work: Microsoft Azure." _What Is a Virtual Machine and How Does It Work | Microsoft Azure_, [azure.microsoft.com/en-us/overview/what-is-a-virtual-machine/](https://azure.microsoft.com/en-us/overview/what-is-a-virtual-machine/)
7. Dataman, Dr. "What Is Image Recognition?" _Medium_, Towards Data Science, 29 Mar. 2020, [towardsdatascience.com/module-6-image-recognition-for-insurance-claim-handling-part-i-a338d16c9de0](https://towardsdatascience.com/module-6-image-recognition-for-insurance-claim-handling-part-i-a338d16c9de0)
8. "But What Is a Neural Network? | Deep Learning, Chapter 1." _YouTube_, YouTube, 5 Oct. 2017, [www.youtube.com/watch?v=aircAruvnKk](http://www.youtube.com/watch?v=aircAruvnKk)
9. Muehlemann, Anton. "How to Train Your Own YOLOv3 Detector from Scratch." _Medium_, Insight, 18 Nov. 2019, [blog.insightdatascience.com/how-to-train-your-own-yolov3-detector-from-scratch-224d10e55de2](https://blog.insightdatascience.com/how-to-train-your-own-yolov3-detector-from-scratch-224d10e55de2)
10. AntonMu. "AntonMu/TrainYourOwnYOLO." _GitHub_, [github.com/AntonMu/TrainYourOwnYOLO](http://github.com/AntonMu/TrainYourOwnYOLO)
11. Microsoft. "Microsoft/VoTT." _GitHub_, [github.com/microsoft/VoTT](https://github.com/microsoft/VoTT)
