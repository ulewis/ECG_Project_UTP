# ECG_Project

## Descripción

Este proyecto tiene como objetivo analizar patrones de arritmias cardíacas mediante el uso de **Tiny ML**. El modelo de Machine Learning ha sido entrenado utilizando la base de datos **MIT-BIH Arrhythmia Database** con TensorFlow. Posteriormente, el modelo entrenado ha sido desplegado en un **NanoArduino** para su implementación en dispositivos de bajo consumo.

### Importante

Este proyecto es **educativo** y **experimental**. **No debe ser utilizado como un método de diagnóstico médico oficial**. No es adecuado para su aplicación en entornos clínicos o médicos. Su propósito es únicamente demostrar el uso de técnicas de Tiny ML para la detección de arritmias en el ámbito de la investigación y la educación.

---

## Estructura del Proyecto

El proyecto está organizado en las siguientes carpetas y archivos:

### 1. **Arduino_TML_ECG**
   - Contiene el código fuente para cargar en un dispositivo Arduino. 
   - Requiere el uso de **Arduino IDE** para cargar el programa en el dispositivo.
   - Incluye el modelo de Tiny ML preentrenado para la detección de arritmias.

### 2. **CppUniteLite** y **UnitTests**
   - Archivos para la simulación y pruebas de los modelos entrenados.
   - **Recomendado para sistemas Linux o macOS**.
   - Esta carpeta es opcional y sirve para probar el rendimiento del modelo sin necesidad de hardware físico.

### 3. **data**
   - Contiene la base de datos utilizada para entrenar el modelo de Machine Learning: **MIT-BIH Arrhythmia Database**.
   - Enlace a la base de datos: [MIT-BIH Arrhythmia Database](https://www.physionet.org/content/mitdb/1.0.0/)

### 4. **tfile-micro**
   - Contiene los archivos del modelo TensorFlow optimizado para microcontroladores (TensorFlow Lite).
   - Este archivo es utilizado para cargar y ejecutar el modelo en dispositivos de baja capacidad, como los **NanoArduinos**.
   - Está basado en Python y es compatible con los archivos de prueba y simulación en **UnitTests**.

---

## Requisitos

- **Hardware**:
  - **NanoArduino** (o similar) para desplegar el modelo.
  
- **Software**:
  - **Arduino IDE** para cargar el código en el dispositivo.
  - **Python 3** para ejecutar los archivos de prueba y simulación.
  - **TensorFlow** (y TensorFlow Lite) para el entrenamiento y optimización del modelo.
  - Sistema operativo recomendado para simulaciones: **Linux** o **macOS**.

---

## Instrucciones de Uso

1. **Preparación del Arduino**:
   - Conecta tu **NanoArduino** a tu computadora.
   - Abre **Arduino IDE** y selecciona el puerto adecuado.
   - Carga los código de la carpeta **Arduino_TML_ECG**.

2. **Entrenamiento del Modelo** (Opcional, si deseas reentrenar el modelo):
   - Utiliza los archivos en la carpeta **data** y las herramientas de TensorFlow para entrenar el modelo con la base de datos MIT-BIH.
   - Exporta el modelo entrenado a formato TensorFlow Lite.

3. **Simulación en PC**:
   - Si no tienes el hardware necesario, puedes simular el modelo en tu PC (Mac o Linux, Windows puede presentar problemático) utilizando los archivos de prueba en la carpeta **CppUniteLite**.

---

## Dudas o problemas

Para reportar problemas o sugerencias, abre un **issue** en el repositorio.


---

## Notas Adicionales

- Este proyecto es con fines educativos y es financiado por la Universidad Tecnológica del Perú
