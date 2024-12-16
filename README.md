This is a simple repository that explains building a calculator using kivy module.

This project follows the tutorial https://thecleverprogrammer.com/2020/12/05/calculator-gui-with-python/ basically and have made some changes.

'Kivy'is an open source library that can be used for implementing user interfaces. Kivy provides different widgets and tools for creating rich, interactive user interfaces, and it supports multi-touch gestures out of the box.

Ás we are using the 'kivy' module for the calculator , we should import its' 'App' module. 

```from kivy.app import App ```

Then let's create a class called MyApp. In this class, we have used 'App' in brackets. That indicates, this MyApp() class inherits from the App class in Kivy module.

```class MyApp(App):```

Next we will create a function called 'build'. We can include the design of the calculator within that function.

``` def build(self):
        root_widget = BoxLayout(orientation='vertical')
        output_label = Label(size_hint_y = 0.75, font_size=50)
        button_symbols = ('1', '2', '3', '+',
                          '4', '5', '6', '-',
                          '7', '8', '9', '.',
                          '0', '*', '/', '=')
        button_grid = GridLayout(cols=4, size_hint_y=2)
        for symbol in button_symbols:
            button_grid.add_widget(Button(text=symbol))

        clear_button = Button(text = 'Clear', size_hint_y=None, height=100)
```

In the above function, we have called the 'BoxLayout' function in Kivy module, to position widgets. There we have used the orientation='vertical', to position widgets above/below. Then we have called the Label function which is also in the Kivy module. There we have configured the 'size_hint_y' which specifies the height that the widget should occupy as a fraction of the available space. At the same time we have passed the 'font_size' of the label. Then we have specify the button symbols of the calculator as a list.

After that we have called the 'GridLayout' function. According to the definition given in the documentation of the 'Kivy' module, 'GridLayout' takes the available space and divides it into columns and rows, then adds widgets to the resulting “cells”.

We have looped the button symbols and for each symbol, when we call add_widget, the 'Button' widget specified inside the parentheses is added to the layout dynamically, at runtime. The text property sets the text that will appear on the button. Next, the 'Clear' button is added to the calculator and its properties are passed as parameters.











