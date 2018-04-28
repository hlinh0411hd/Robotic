# Robotic

## Setting up
Copy folder custom vao thu muc "gym_gazebo/envs"
Copy folder launch, models, worlds vao thu muc "gym_gazebo/envs/assets". skip nhung file trung
Copy fild __init__.py vao trong thu muc "gym_gazebo" (copy de)

vao trong thu muc "gym_gazebo/envs/assets/launch", mo file MazeColor.launch, sua truong defaul o
"<arg name="world_file"  default="/home/hlinh0411hd/gym-gazebo/gym_gazebo/envs/installation/../assets/worlds/maze_color.world"/>"
tro toi file "maze_color.world" trong folder "worlds"


## Running
Vao trong folder "ForLearn", chay lenh terminal "python DeepQlearningWithEgreedy.py"

## Information

### Moi truong:
	Target la hinh tru do
	Hint la cac vong tron nhieu mau
	Nhiem vu la cho turtlebot hoc cach di chuyen den target


### file: gazebo_turtlebot_maze_color.py trong thu muc custom
	file dinh nghia moi truong
	+ hien tai dang tra ve observation la 3 gia tri: anh mau RGB(32*32*3), laserscaner, va position cua turtlebot
	+ reward: 200 khi cham den dich, -200 khi dam vao tuong, 10 khi cham lan dau tien vao hint
	+ action: gom 5 action: 2 re trai, 1 di thang, 2 re phai


### file: DeepQLearingWithEgreedy.py trong thu muc ForLearn:
	file training: dang cai dat thuat toan Q-learning voi E-greedy

### file: ExperienceReplay.py trong thu muc ForLearn:
	class chua cac experiences cua turtlebot

### file: Qnetwork.py trong thu muc Forlearn:
	class Qnetwork:
		thong tin ve mang neural network
		co mot so ham ho tro

	Viec thay doi cau truc mang neural network dc thay doi trong file nay

### file: Ultility.py trong thu muc Forlearn
	cac class ho tro viec luu du lieu va luu cac thong so


## Note
	Co the su dung 1 hoac ca 3 du lieu dua ra tu environment
	viec thay doi cau truc mang, thuat toan dc sua trong file Qnetwork.py
	viec thay doi strategy chon action dc thay doi trong file DeepQlearing...
	viec thay doi cac du lieu moi truong trong file gazebo_turtlebot_maze_color.py
	thay doi thong so trong file Ultility.py

	###Hien tai co 3 target trong moi truong duoc random trong moi lan chay
	cac hint duoc tinh diem tai lan dau tien cham phai