<!DOCTYPE html>
<html>



https://github.com/Dania003/Car-Detector/assets/69827478/633c580d-99ab-48af-a18c-fe0d5d3a68d9


<body>
	<div class="container">
		<h1>Car-Detector</h1>
		<h2>Background:</h2>
		<p>TMMC has vision systems on assembly line conveyors to perform vehicle quality checks. These vision systems require input from the conveyor to know when a car enters the vision station. Moreover, the vision system has multiple cameras, and each camera is required to be triggered at a certain position as the car traverses through the vision station.</p>
		<p>Currently, the vision system triggers are not consistent which causes variation in images and causes false fails. To get consistent images, cameras need to be triggered precisely and repeatably when the car is in position. The assembly shop has different lines. Each line consists of fixed length pitches. The vehicles in the pitches can be of different lengths (multi model). Currently, the vision system uses a line encoder but due to the communication delays and some mechanical issues (such as in the carriers rocking), the vision does not precisely know the position of vehicle.</p>
		<h2>Problem:</h2>
		<p>In order to solve this problem, we used python to build a program that acts as a vehicle detector from visual input. Using OpenCV, we were able to analyze and read visual information!</p>
		<p>The issue we were facing was that OpenCV could only detect regular shapes; cars are not really regular in shape…. But their wheels are! Obviously, the wheels are always circular! This means that OpenCV could always detect the wheels. Since we were working specifically with Toyota cars; thus we knew the dimensions of its specific parts such as the radius of its wheels. Thus, we were able to specify to the program what circles to look for (we don’t want the program to look for circles that are not wheels). By detecting one of the wheels (specifically the front right wheel) as a circle, we were able to store the location of it in an array meaning that we were able to detect its position at any point of time! Since we know the dimensions of the car, we were able to draw a border rectangle that traces the car as it moves all depending on the location of the wheel!</p>
		<h2>How does it work?</h2>
  


https://github.com/Dania003/Car-Detector/assets/69827478/feb9aeb5-a96c-45e1-b80a-c7d84df4cea5



