-- Descripción
Compilador realizado para la clase de Arquitectura de computadores. Fue diseñado para el computador de propósito general hecho en clase. Convierte un programa en lenguaje ensamblador a binario (realmente a hexadecimal, porque se usa para un proyecto en ISE). 
Se hizo tomando como ejemplo el siguiente tutorial: 
  https://blog.usejournal.com/writing-your-own-programming-language-and-compiler-with-python-a468970ae6df
en el cual se hace uso de la biblioteca rply.

--USO
Desde la línea de comandos escribir
  python cli.py "nombre.txt"
o si se usa con el ejecutable
  compilador.exe "nombre.txt"
El archivo "nombre.txt" debe estar en la carpeta del compilador (a no ser que el ejecutable esté en el PATH)
Se generarán 2 archivos:
  "nombre - Binary code.txt" -> Archivo que contiene directamente la traducción a código hexadecimal de 16 bits
  "nombre - initRam.coe" -> Archivo para los proyectos en ISE
  
En lenguaje ensamblador las etiquetas deben iniciar con @ y se admiten comentarios que deben iniciar con %.
  
--Comando para compilar con pyinstaller
pyinstaller cli.py --name compilador --paths compilador --hidden-import rply --hidden-import abs_syn_tree --hidden-import lexer --hidden-import parce -F
