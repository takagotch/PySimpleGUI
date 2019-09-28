### pysimplegui
---
https://github.com/PySimpleGUI/PySimpleGUI

```py
// ProgrammingClassExamples/Win10 versions/2b_makewinexe_file.py
import PySimpleGUI as sg
sg.ChangeLookAndFeel('GreenTan')
sg.SetOptions (font=('callbri',12,'bold') )

form = sg.FlexForm('Gym Membership')

layout = [[sg.Text('Membership Calculator', font = ('Calibri', 16, 'bold'))],
    [sg.Checkbox('CGS student?', size = (22,1)),
      sg.ReadButton('Display Cost', size = (14,1))],
    [sg.Radio('One Month', 'Radio1', default = True),
      sg.Radio('Three Month', 'Radio1'),
      sg.Radio('One Year', 'Radio1')],
    [sg.Text('', size = (30,1), justification = 'center', font =('Calibri', 16, 'bold'), key = 'result')]]

form.Layout(layout)
while True:
  button, value = form.Read()
  if button is not None:
    if value[1]:
      cost = 50
    elif value[2]:
      cost = 100
    else:
      cost = 300
    if value[0]:
      cost = cost*0.9
    result = str('Cost: ' + '$(:.2f)'.format(cost))
    form.FindElement('result').Update(result)
  
  else:
    break
```

```
```

```
```


