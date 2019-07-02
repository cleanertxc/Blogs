# 1. Function
1. 打开网页
import webbrowser
webbrowser.open("URL")
2. 挂起程序
import time
time.sleep(10(s))
3. 找到指定地址的所有文件名
import os
file_list=os.listdir(r"C:\Users\xichentan\Downloads\prank\prank")
#r 表示rawpack，表示r之后的内容只能解释为字符串形式
4. 文件重命名
os.rename(oldname,newname)
# 2. Classes
Class is like a blueprint and its object is like an instance of the blueprint.
 >`def __init__()` initializes or creates space in memory for a new instance.
 - 使用jupyter在导入目录下的其他`.ipynb`文件时，需要重新将其download as `.py`后缀文件才可以在其他的`.ipynb`文件中import.
```python
import webbrowser
#Class
class Movie():
    #Constructor
    def __init__(self,movie_title,movie_storyline,poster_image,trailer_youtube):
        #Instance Variables
        self.title=movie_title
        self.storyline=movie_storyline
        self.poster_image_url=poster_image
        self.trailer_youtube_url=trailer_youtube
    #Instance Methods
    def show_trailer(self):
        webbrowser.open(self.trailer_youtube_url)
```
# 3.Inheritance
```python
class Parent():
	def __init__(self,last_name, eye_color):
		print("Parent Constructor Called")
		self.last_name=last_name
		self.eye_color=eye_color
	def show_info(self):
			print("Last Name - "+self.last_name)
			print("Eye Color - "+self.eye_color)
			
class Child(Parent):
	def __init__(self,last_name, eye_color, number_of_toys):
		print("Child Constructor Called")
        Parent.__init__(self,last_name,eye_color)
        self.number_of_toys=number_of_toys
		def show_info(self):
			print("Last Name - "+self.last_name)
			print("Eye Color - "+self.eye_color)
			#Method Overriding
			print("Number of toys - "+str(self.number_of_toys))

billy_cyrus=Parent("Cyrus","Blue")
miley_cyrus=Child("Cyrus","Blue",5)
```
