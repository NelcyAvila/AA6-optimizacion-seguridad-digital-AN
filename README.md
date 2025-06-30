# Parte 2: Taller técnico en Python

El objetivo es aprender cómo proteger información personal, como nombres, correos, contraseñas y diagnósticos, usando herramientas en Python.

En el taller se aplicaron técnicas como cifrado, hash y pseudonimización en datos de pacientes de un hospital, estas técnicas son comunes cuando se trabaja con datos confidenciales en la vida real.
### 1. Se creó la base de datos

Se creó la base de datos con datos de 4 pacientes que contienen los campos de D, nombre_completo, correo, edad, diagnóstico,
contraseña.

## 2. Tecnicas implementadas

### Cifrado de datos sensibles

Primero, se cifraron dos columnas del archivo: el **correo electrónico** y el **diagnóstico médico**. Esto se hizo usando la librería cryptography y el método Fernet. Lo cual significa que esa información queda protegida y no se puede leer directamente, a menos que se tenga una clave secreta.

Esto es muy útil si se trabaja con datos reales, porque si alguien se roba el archivo, no podrá leer el contenido si no tiene esa clave.

### Pseudonimización del nombre y del correo

Después, se aplicó la pseudonimización, que sirve para ocultar información identificable. En este caso se usó el algoritmo SHA-256, que convierte los datos en cadenas largas de números y letras, es decir, un hash. Mediante ello es imposible volver al valor original, por lo que protege la identidad de la persona.

Se aplicó esta técnica al nombre completo y al correo cifrado. cabe reclacar que aunque el correo ya estaba cifrado, se añade una capa más de cifrado, lo cual aumenta la seguridad.

### Hash seguro de contraseñas

Aquí en lugar de guardar las contraseñas reales, se aplicó bcrypt, que es un método de hash. Esto convierte las contraseñas en códigos que no se pueden descifrar. Aunque otra persona vea esos códigos, no sabrá qué contraseña usaba la persona originalmente.

Esta técnica es muy común en páginas web y aplicaciones donde los usuarios deben ingresar contraseñas.

### Control de acceso con contraseña

Por último, se añadió un pequeño control de acceso. Antes de mostrar los datos protegidos de los pacientes, el programa pide que el usuario escriba una contraseña. Si escribe la correcta, se muestran los datos, caso contrario se bloquea el acceso y se muestra un mensaje de contraseña incorrecta. Este paso ayuda a entender cómo funcionan los sistemas que protegen el acceso a información privada de los pacientes, en este caso.

Todas estas técnicas se usan para proteger datos personales, en este caso se realizó una simulación con pacientes de hospitales, pero tambien aplica a universidades o bancos. Mediante este ejemplo se puede evidenciar que en la vida real, si los datos de una persona no tienen protección y se fiultran se filtran puede haber consecuencias legales y éticas muy graves. Por ejemplo, se puede violar la privacidad, causar discriminación o incluso usarlos para fraudes.

## Instrucciones para ejecutar elcódigo
 1. Abre el archivo `AA6_Avila_Nelcy_Taller_Python.ipynb` en Google Colab o Jupyter Notebook.

 2. Asegúrate de instalar las librerías necesarias, en este caso las que se usaron son:
    -import pandas as pd
    -from cryptography.fernet import Fernet
    -import hashlib
    -import bcrypt
Ejecuta las celdas en orden de acuerdo alcódigo realizado, empezando de laparte superior.

En laparte final, en la que te pide la contraseña usa esta: accesopaciente2025
Y listo. 

    
   

