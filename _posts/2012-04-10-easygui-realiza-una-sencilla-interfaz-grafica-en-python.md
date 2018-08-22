---
layout: post
title: "EasyGui: Realiza una sencilla interfaz gráfica en Python"
date: 2012-04-10 21:32:00 +0200
categories: Desarrollo
---
Como su propio nombre indica **EasyGui** es un módulo muy simple, para la programación de una interfaz gráfica en Python.

![Logotipo de Python]({{"/assets/img/posts/2012/04/python-logo.png" | absolute_url }}){: .img-responsive .margin-auto }
  
No requiere ningún tipo de conocimiento añadido, todas las interacciones de la interfaz son realizadas mediante llamadas a funciones simples.

A continuación dejo una breve chuleta con algunas de las cosas que podemos hacer:

{% highlight python %}
# Display a msgbox with choices of Yes and No.
ynbox(msg='Shall I continue?', title='', choices=('Yes','No'), image=None)

# Display a msgbox with choices of Yes and No.
ccbox(msg='Shall I continue?', title='', choices=('Continue','Cancel'), image=None)

# Display a msgbox with choices of Continue and Cancel.
boolbox(msg='Shall I continue?', title='', choices=('Yes','No'), image=None)

# Display a boolean msgbox.
indexbox(msg='Shall I continue?', title='', choices=('Yes','No'), image=None)

# Display a buttonbox with the specified choices.
msgbox(msg='(Your message goes here)', title='', ok_button='OK', image=None, root=None)

# Display a messagebox.
buttonbox(msg='', title='', choices=('Button1','Button2','Button3'), image=None, root=None)

# Display a msg, a title, and a set of buttons.
integerbox(msg='', title='', default='', lowerbound=0, upperbound=99, image=None, root=None, **invalidKeywordArguments)

# Show a box in which a user can enter an integer. 
multenterbox(msg='Fill in values for the fields.', title='', fields=(), values=())

# Show screen with multiple data entry fields. 
multpasswordbox(msg='Fill in values for the fields.', title='', fields=(), values=())

# Same interface as multenterbox.
enterbox(msg='Enter something.', title='', default='', strip=True, image=None, root=None)

# Show a box in which a user can enter some text. 
passwordbox(msg='Enter your password.', title='', default='', image=None, root=None)

# Show a box in which a user can enter a password.
multchoicebox(msg='Pick as many items as you like.', title='', choices=(), **kwargs)

# Present the user with a list of choices.
choicebox(msg='Pick something.', title='', choices=())

# Show easygui revision history
abouteasygui()

{% endhighlight %}
    
Para usar EasyGUI, simplemente basta con copiar el archivo <i>easygui.py</i> en la carpeta donde tenemos nuestro programa de Python.

Descargar [EasyGUI v. 0.96](http://easygui.sourceforge.net/download/version_0.96/index.html#downloadFiles)
 