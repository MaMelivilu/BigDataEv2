# Proyecto: Avistamientos OVNI

Este proyecto documenta paso a paso el procesamiento de datos de avistamientos de OVNIs utilizando herramientas de Google Cloud Platform, como Cloud Storage, BigQuery, Dataprep y Looker Studio.

---

## 1. Acceso al laboratorio

Se inicia el laboratorio, donde se nos entregan las credenciales para acceder al entorno de GCP.

![Credenciales](https://github.com/user-attachments/assets/b91f10f5-c15e-4695-80d4-c342764a68b0)

---

## 2. Creación del bucket en Cloud Storage

Ingresamos con las credenciales proporcionadas, accedemos al proyecto y creamos un bucket llamado `giovanni-matias`.

![Creación del bucket](https://github.com/user-attachments/assets/ce678bb2-45d4-4f09-9669-c239d2a8cc60)

Vista del bucket una vez creado:

![Bucket creado](https://github.com/user-attachments/assets/3d81eea6-6e40-4853-97b2-133b1c895430)

---

## 3. Creación del Dataset en BigQuery

Creamos un dataset en BigQuery con el nombre `ovni`.

![Creación del dataset](https://github.com/user-attachments/assets/a2a05a2e-0f12-48ab-a506-92a4ddc301ec)

#### Vista de la creación del dataset en el proyecto
![Vista del dataset](https://github.com/user-attachments/assets/3590bc07-0962-4c5f-8e8d-c8fda5073ef4)


---

## 4. Uso de Dataprep y creación del Flow

Accedemos a Dataprep y creamos un flow llamado `Avistamientos`.

![Flow creado](https://github.com/user-attachments/assets/2d8b062a-6b09-4040-87df-f1144cf2f719)

---

## 5. Carga del archivo CSV

Transformamos el archivo original de formato `.xlsx` a `.csv` y lo cargamos en el flow.

![Carga del CSV](https://github.com/user-attachments/assets/c9a7af8c-92af-4367-9e96-757f50e46d44)

Estructura del flow luego de la carga:

![Estructura del flow](https://github.com/user-attachments/assets/889f3269-d9e0-4331-9886-b89607800e87)

---

## 6. Revisión del contenido del CSV

Verificamos que todos los datos se hayan cargado correctamente en Dataprep.

![CSV cargado](https://github.com/user-attachments/assets/64a96e0f-cccf-4e64-be4b-d7a83fdb8d23)

---

## 7. Limpieza de los datos

Eliminamos registros vacíos o inconsistentes para preparar el archivo.

![Limpieza de datos](https://github.com/user-attachments/assets/60d9313c-87f3-443c-ac98-60a848daea16)

Vista de la tabla limpia:

![Tabla limpia](https://github.com/user-attachments/assets/9fc4cb6a-3dde-40c3-8b5b-36d45f5a8b98)

---

## 8. Ejecución del Flow

Ejecutamos el Flow para aplicar los cambios.

![Run flow](https://github.com/user-attachments/assets/9c049603-c275-4644-a6f0-9240dcb094b8)

---

## 9. Exportación del CSV limpio

Extraemos el archivo CSV procesado y lo subimos nuevamente al bucket `giovanni-matias`.

![Subida al bucket](https://github.com/user-attachments/assets/eac7becb-2751-4ff7-b7d3-c7d780e7ab36)

---

## 10. Creación de la tabla en BigQuery

Creamos la tabla `avistamientos` en el dataset `ovni`.

![Tabla creada](https://github.com/user-attachments/assets/1e46bd2f-6d48-433f-a085-552db39c1018)

Tuvimos un inconveniente con la primera tabla, por lo que se debió crear una nueva.

![Vista previa](https://github.com/user-attachments/assets/e135b4ad-af57-4c4f-9541-7dae55ac0455)

---

## 11. Consultas SQL de validación

Ejecutamos las siguientes 3 consultas para validar los datos cargados:

### Consulta 1  
![Consulta 1](https://github.com/user-attachments/assets/4b1a364c-6cdd-4a25-af6e-f63ecc3d0d42)

### Consulta 2  
![Consulta 2](https://github.com/user-attachments/assets/ad169881-b921-4b4c-820c-ad5c1fceb79d)

### Consulta 3  
![Consulta 3](https://github.com/user-attachments/assets/112dfe9b-1137-4d7a-bdd1-15dcd11ee72c)

---

## 12. Visualización de resultados en Looker Studio

Transformamos los resultados de las consultas en gráficos utilizando Looker Studio:

- **Consulta N°1**  
  ![Gráfico 1](https://github.com/user-attachments/assets/a00c7d12-fbd6-462e-906c-9761f0d41b13)

- **Consulta N°2**  
  ![Gráfico 2](https://github.com/user-attachments/assets/a98acdc7-0899-4da0-984a-97e9e076335b)

- **Consulta N°3**  
  ![Gráfico 3](https://github.com/user-attachments/assets/ff761e12-19b8-4519-95d7-91e14256e324)

---






   
