---
Established: 2024-12-29
Last Updated: 2025-01-08
Description: Questions about letting a model to emit signal while it is updated.
tags:
  - python
  - GUI
  - Question
  - Resolved
  - MVC
---
# Sources
> [!cite]
> Type: Book
> Title: Create GUI Application with Python & Qt6: The hands-on guide to making apps with Python
> Location_1: Page 298-299, Listing 108. further/mvc_5.py, Chapter:19
> Location_2: Page 603-604, Listing 258. further/signals_custom.py, Chapter 35
> 

To use "Signals and Slots" so that a model can emit a signal (like string, numbers, list, dictionary, etc.), in chapter 18, the example additionally defined a class DataModelSignals which inherit the "Signals and Slots" from class QObject. In this way, the instance, a customized model produced by the class UserDict, which is not a subclass of QObject (no "Signals and Slots") can define a signal through the instance of class DataModelSignals.

```python title="Listing 108. further/mvc_5.py"
from collections import UserDict

# Need to addtionally define the class DataModelSignals which inherit QObject
class DataModelSignals(QObject):
	# Emit an "updated" signal when a property changes.
	updated = Signal()
	
# The actual class produce instances of models
# UserDict is not a subclass of QObjects
class DataModel(UserDict):
	def __init__(self, *args, **kwargs):
		# An instance from class DataModelSignals which have signals and slots
		self.signals = DataModelSignals()
		super().__init__(*args, **kwargs)
		
	def __setitem__(self, key, value):
		# Get the existing value.
		previous = self.get(key) # Returns None if key not set.
		super().__setitem__(key, value) # Set the value.
		if value != previous: # There is a change.
			self.signals.updated.emit() # Emit the signal.
			print(self) # Show the current state.
```

In contrast, in Chapter 35, the class MainWindow which inherit the properties and methosds of QMainWindow is a subclass of QObject. Therefore, the "Signals and Slots" can be used directly.
```python title="Listing 258. further/signals_custom.py"
import sys
from PySide6.QtCore import Signal
from PySide6.QtWidgets import QApplication, QMainWindow

class MainWindow(QMainWindow):
	# The class can use Signal function directly
	message = Signal(str) ①
	value = Signal(int, str, int) ②
	another = Signal(list) ③
	onemore = Signal(dict) ④
	anything = Signal(object) ⑤

	def __init__(self):
		super().__init__()
		self.message.connect(self.custom_slot)
		self.value.connect(self.custom_slot)
		self.another.connect(self.custom_slot)
		self.onemore.connect(self.custom_slot)
		self.anything.connect(self.custom_slot)
		self.message.emit("my message")
		self.value.emit(23, "abc", 1)
		self.another.emit([1, 2, 3, 4, 5])
		self.onemore.emit({"a": 2, "b": 7})
		self.anything.emit(1223)
		
	def custom_slot(self, *args):
		print(args)

app = QApplication(sys.argv)
window = MainWindow()
window.show()
app.exec()
```

> [!seealso]
> [Signals and Slots - Qt for Python](https://doc.qt.io/qtforpython-6/tutorials/basictutorial/signals_and_slots.html)
> [Questions about MVC - q&a - Python GUIs Forum](https://forum.pythonguis.com/t/questions-about-mvc/1704)
