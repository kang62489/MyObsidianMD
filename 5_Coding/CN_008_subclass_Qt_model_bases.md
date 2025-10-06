---
Established: 2025-01-08
Last Updated: 2025-01-08
Description: Caution of define a custom model by subclassing from a base implementation
tags:
  - python
  - GUI
  - MVC
---
# Sources
> [!cite]
> Type: Book
> Title: Create GUI Application with Python & Qt6: The hands-on guide to making apps with Python
> Location_1: Page 316-320, Listing 129. model-views/todo_1b.py, Chapter:21
> Location_2: Page 331-332, Listing 127. model-views/tableview_demo.py, Chapter 22
> 

```python title="Listing 120. model-view/todo_1b.py"
import sys
from PySide6.QtCore import QAbstractListModel, Qt
from PySide6.QtWidgets import QApplication, QMainWindow

# Remove "from MainWindow import Ui_MainWindow"
# I use pathlib and importlib to use the ui file in the folder of example codes
# =============================================================================
import importlib.util
from pathlib import Path
base_path = Path("D:\\Programs")
dir_path = Path("Python\\create-gui-applications-pyside6\\model-views")
ui_path = base_path / dir_path / "MainWindow.py"
print(ui_path)
spec = importlib.util.spec_from_file_location("MainWindow", ui_path.resolve())
mod = importlib.util.module_from_spec(spec)
sys.modules["MainWindow"] = mod
spec.loader.exec_module(mod)
Ui_MainWindow = mod.Ui_MainWindow
# ==============================================================================

class TodoModel(QAbstractListModel):
	def __init__(self, todos=None):
		super().__init__()
		self.todos = todos or []
	def data(self, index, role):
		if role == Qt.DisplayRole:
			status, text = self.todos[index.row()]
			return text
	def rowCount(self, index):
		return len(self.todos)
	
class MainWindow(QMainWindow, Ui_MainWindow):
	def __init__(self):
		super().__init__()
		self.setupUi(self)
		self.model = TodoModel()
		self.todoView.setModel(self.model)
		
app = QApplication(sys.argv)
window = MainWindow()
window.show()
app.exec()



```

> [!info] 
> The example code above is modified to make it able to import classes or modules from a python file which located in another directory
> - To make it can load the the python file of ui (compiled ui file)

As the example above shown, to define our customized data model by subclassing Qt implementation bases. There are some methods must be defined. Here, for subclassing QAbstractListModel, the data() and rowCount() must be predefined to override the methods inherit from the class. Besides, the parameter "index" and "role" are build-in methods inherit from the QAbstractListModel as well, therefore the view can call the "data" method by passing the index and role objects through request.

Similarly in the example code of Listing 127, the implementation must have are data(), rowCount(), and columnCount()
```python title="Listing 258. further/signals_custom.py"
import sys
from PySide6.QtWidgets import QMainWindow, QApplication, QTableView
from PySide6.QtCore import Qt, QAbstractTableModel

class TableModel(QAbstractTableModel):
	def __init__(self, data):
		super().__init__()
		self._data = data
		
	def data(self, index, role):
		if role == Qt.DisplayRole:
		# See below for the nested-list data structure.
		# .row() indexes into the outer list,
		# .column() indexes into the sub-list
			return self._data[index.row()][index.column()]
		
	def rowCount(self, index):
		# The length of the outer list.
		return len(self._data)
		
	def columnCount(self, index):
		# The following takes the first sub-list, and returns
		# the length (only works if all rows are an equal length)
		return len(self._data[0])
class MainWindow(QMainWindow):
	def __init__(self):
		super().__init__()
		self.table = QTableView()
		data = [
		[4, 1, 3, 3, 7],
		[9, 1, 5, 3, 8],
		[2, 1, 5, 3, 9],
		]
		
		self.model = TableModel(data)
		self.table.setModel(self.model)
		self.setCentralWidget(self.table)
		
app = QApplication(sys.argv)
window = MainWindow()
window.show()
app.exec()
```

> [!seealso]
> [QAbstractListModel - Subclassing](https://doc.qt.io/qtforpython-6/PySide6/QtCore/QAbstractListModel.html#subclassing)
> [QAbstractTableModel - Subclassing](https://doc.qt.io/qtforpython-6/PySide6/QtCore/QAbstractTableModel.html#subclassing)
