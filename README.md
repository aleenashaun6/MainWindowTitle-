# MainWindowTitle-
Get-Process |      Where-Object {$_.MainWindowTitle -like "*notepad*"} |          Select MainWindowTitle, MainWindowHandle |             Out-GridView If you're looking to capture more like all open windows, you can modify it slightly:  Get-Process |     Where-Object {$_.MainWindowTitle -ne ""} |         Select MainWindowTitle, MainWindowHandle |             Out-GridView
