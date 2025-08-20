# good-seed-edad-prediccion
Predicción de edad utilizando ResNet50 para ayudar a los supermercados Good Seed a cumplir con las regulaciones de venta de alcohol a menores.
# 🛒 Good Seed – Age Prediction with Computer Vision  

## 📌 Descripción del proyecto  
La cadena de supermercados **Good Seed** busca cumplir con la normativa sobre la venta de alcohol, asegurándose de no vender a menores de edad. Para ello, se planteó el uso de **cámaras en las cajas registradoras** junto con un modelo de **visión por computadora** que estime la edad de los clientes a partir de imágenes.  

Este proyecto implementa una **red neuronal convolucional (CNN)** basada en **ResNet50** para predecir la edad de una persona en años a partir de fotografías.  

---

## 🛠️ Tecnologías utilizadas  
- Python (Pandas, NumPy, Matplotlib)  
- TensorFlow / Keras  
- ResNet50 (transfer learning)  
- Google Colab  

---

## 📂 Estructura del repositorio  
- `notebooks/` → notebook con el desarrollo del modelo.  
- `reports/` → resultados exportados en `.html` y `.pdf`.  
- `src/` → scripts con funciones para carga de datos, creación y entrenamiento del modelo.  
- `README.md` → documentación principal del proyecto.  

---

## 📊 Resultados del modelo  

- Conjunto de entrenamiento: **6073 imágenes**  
- Conjunto de validación: **1518 imágenes**  

**Métricas principales (época 5/5):**  
- **Pérdida (loss):** 285.26  
- **MAE (error absoluto medio):** 12.93 

📌 El modelo logra una precisión aceptable para la estimación de edad, con un error promedio de ~13.  

---

## 🚀 Flujo de trabajo  

### 1. Carga y preparación de datos  
Se cargaron las imágenes y etiquetas de edad desde `labels.csv`. Los datos se dividieron en **80% entrenamiento** y **20% validación**, aplicando normalización con `ImageDataGenerator`.  

### 2. Creación del modelo
Se utilizó ResNet50 como modelo base (preentrenado en ImageNet) con capas adicionales para regresión:

### 3. Entrenamiento
El modelo se entrenó durante 5 épocas en Colab (GPU activada).

👩‍💻 Autor

Rita María de la Luz Morales Hernández

train_data = load_train(path)
test_data = load_test(path)
