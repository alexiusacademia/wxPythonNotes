# wxPython Notes

A collection of notes during my study of the Python GUI framework, wxPython.

























Author:

#### ALEXIUS S. ACADEMIA

<div style="page-break-after: always;"></div>
# Introduction

	Due to the simplicity in coding using the Python language, I have decided to use it as the main tool/language for building desktop applications (or maybe web applications as well) for my company products and projects or for side projects. 

	Good thing about Python is that it comes with it's own Graphical User Interface (GUI) toolkit, _tkinter_. Now after learning the basic and some advanced stuffs and building a few applications with it as the GUI toolkit, I've come to realize that tkinter was great for basic and simple projects, but lacks some essential features out of the box for building complex desktop applications like database tools, printing functionality and print preview, easy support for multiple document interface, etc.

	Now this doesn't mean that these said features cannot be implemented while using _tkinter_, it's just that it would take a lot of work to do so and we all know that time is essential for any project. So after realizing this, I tried to look for the alternatives and there's a lot of them actually.

	The trick by the way when choosing an alternative is that you don't have to try and check them all, you just go with those that comes to the top of the list in terms of popularity and functionality. Usually, those will be your preferred options anyway after testing them all. 

	Now, after checking out the two most popular, wxWidgets and QT, I thought I'd go with wxWidgets which has a Python binding wxPython. They are both great, the only downside of QT for me is that it's free to use as long as you're creating open source applications, aside from that, you'd have to pay for a license. This doesn't sound good for me at least so I decided to go with wxPython.

<div style="page-break-after: always;"></div>

# Anatomy of a wxPython Application

​	Now to dive in to the topic, the following presents the basic content of a wxPython application.

```python
import wx


class MainFrame(wx.Frame):
    def __init__(self, parent=None):
        # Now this is where you'd want to put the codes for your user interface in a  
        # frame. Let's pass in for now
        pass
    
    
class MyApp(wx.App):
    def OnInit(self):
        main_frame = MainFrame()
        main_frame.Show()
        return True
    
if __name__ == '__main__':
    app = MyApp()
    app.MainLoop()
```

