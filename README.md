# Instruccciones de despliegue

Instale las dependencias

```bash
pip install fastapi
pip install "uvicorn[standard]" 
```

Corra el servidor

```bash
uvicorn main:app --reload
```

# Instrucciones de uso

El endpoint de la API es `http://localhost:8000/`

## Ejemplo de uso

Para el endpoint de `/predict` se debe enviar un JSON con la siguiente estructura:

```json
{
  "year": 2002,
  "km_driven": 0,
  "seats": 5,
  "max_power": 20,
  "fuel": "Diesel",
  "transmission": "Automatic"
}
```

# Pruebas

Las pruebas de postman se encuentran en el archivo `tests.postman_collection.json`, se puede importar en postman y ejecutar las pruebas.

# Demás 

Para mitigar incoherencias en la predicción se puede utilizar un modelo de regresión lineal, que permita predecir el precio de un vehículo con mayor precisión. 