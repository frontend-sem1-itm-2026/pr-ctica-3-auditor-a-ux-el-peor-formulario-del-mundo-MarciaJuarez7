En este archivo debes **listar los problemas encontrados** en el formulario.

Se recomienda clasificar los hallazgos usando las siguientes categorías:

### Categorías sugeridas

**UX (Experiencia de usuario)**  
- claridad del flujo  
- botones confusos  
- acciones poco claras  

**Accesibilidad**  
- falta de labels  
- bajo contraste  
- problemas de navegación  

**Validación**  
- campos sin validación  
- tipos incorrectos  
- campos que deberían ser `required`  

**Jerarquía visual / Layout**  
- orden incorrecto  
- agrupación deficiente  
- mala organización de campos  

**Responsive**  
- problemas en pantalla móvil  
- layout que se rompe  
- elementos demasiado grandes o pequeños  

**Contenido**  
- textos confusos  
- requisitos absurdos  
- instrucciones poco claras  

---

# 📊 Formato recomendado

Puedes usar una tabla como esta:

| # | Problema detectado | Categoría | Evidencia | ¿Por qué es un problema? |
|---|---|---|---|---|
| 1 | El campo nombre no tiene label | Accesibilidad | Campo “Nombre” | Los lectores de pantalla no pueden interpretarlo correctamente |
| 2 | Botón cancelar junto al enviar | UX | Botones al final | Puede provocar errores al usuario |
| 3 | Confirmar correo es opcional | Validación | Campo email | Puede causar inconsistencias |

Se recomienda identificar **al menos 10 problemas**.

---

# 📸 Evidencia visual

Además del archivo `AUDITORIA.md`, debes agregar **capturas de pantalla** del formulario.

Incluye al menos:

### 1️⃣ Vista en escritorio
Ventana normal del navegador.

### 2️⃣ Vista en móvil
Ventana reducida o modo responsive del navegador.

Puedes nombrarlas por ejemplo:
captura-escritorio.png
captura-movil.png

---
# 🚫 Regla importante

❌ **No debes modificar el HTML o CSS del formulario.**  

Esta actividad es únicamente de **análisis y auditoría**.
---

# 📦 Entrega

Realiza un **commit en tu repositorio** que incluya:

AUDITORIA.md
captura-escritorio.png
captura-movil.png


Mensaje de commit sugerido:
Auditoría UX del formulario: identificación de problemas de diseño


---

# 💡 Consejo

Piensa como un **usuario real** que intenta completar el formulario.

Si algo te confunde, probablemente **también confundirá a otros usuarios**.

 RESULTADOS:

| # | Problema detectado | Categoría | Evidencia | ¿Por qué es un problema? |
|---|-------------------|-----------|-----------|--------------------------|
| 1 | Falta meta viewport | Responsive | Línea 7 comentada: <!-- <meta name="viewport"... --> | En móvil todo se ve pequeño, el usuario tiene que hacer zoom manualmente |
| 2 | Campos sin label, solo placeholders | Accesibilidad | Todos los inputs tienen placeholder pero no <label> | Lectores de pantalla no pueden identificar los campos correctamente |
| 3 | Texto de ayuda con bajo contraste | Accesibilidad | Clase .low-contrast con color #d3d3d3 | Casi no se lee el texto, usuarios con problemas de visión no pueden verlo |
| 4 | Botón "Borrar todo" junto al de guardar | UX | Botón rojo al final del formulario | Seria mas innecesario el tener si ya tenemos un boton para cancelar el formulario |
| 5 | Campo de fecha como tipo text | Validación | <input type="text"> para fecha de nacimiento | Usuario puede escribir cualquier cosa, no hay validación de formato |
| 6 | Campo que mezcla 3 datos diferentes | UX / Contenido | "Nacionalidad, religión y estado civil" en un solo input | La informacion que se solicita no es coherente o logico entre si y al mismo tiempo pedir requisitos innecesarios como lo es la religion |
| 7 | Confirmación de correo sin validación | Validación | Dos campos de email pero no verifican que sean iguales | Pueden haber errores de dedo y el usuario no lo sabe |
| 8 | Teléfonos como tipo text | Validación | Inputs de teléfono con type="text" | Se esta solicitando como tipo de texto y no de numero |
| 9 | Select de país con opciones insuficientes | UX | Solo "México" y "Otro" | Si eres de otro país, "Otro" no es útil ya que no especifica o representa algun otro pais |
| 10 | Requisitos de contraseña confusos | Contenido | "Jeroglíficos y buena vibra" como requisito | No es claro, "buena vibra" no es un criterio logico o con sentido para lo que se pide asi mismo como los Jeroglíficos |
| 11 | Textarea que exige 500 palabras | UX / Validación | "Describe en al menos 500 palabras" | Nadie va a escribir 500 palabras para registrarse |
| 12 | Checkboxes con textos coercitivos | Contenido | "Acepto términos que no he leído" y "Confirmo aunque no lo sé" | Obliga al usuario a mentir, problemas éticos y legales |
| 13 | Formulario demasiado angosto | Layout | Columna col-md-5 en escritorio | Se desperdicia espacio, parece una tira delgada en pantallas grandes |
| 14 | Campos de dirección desorganizados | Jerarquía visual | Calle, números, colonia sin agrupación clara | No cuenta con una jerarquia logica al pedir datos de la vivienda |
| 15 | Mensaje de error poco útil | Contenido | "No se mostrarán detalles del error" | Usuario no sabe que es lo que debe de corregir y tambien es muy poco claro a la vista siendo casi imperceptible |