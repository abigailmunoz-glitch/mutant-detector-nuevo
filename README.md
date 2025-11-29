---

```markdown
#  Mutant Detector - Proyecto Mejorado

---

##  Descripción

Proyecto mejorado y completo que detecta si un humano es mutante basándose en su secuencia de ADN mediante una API REST construida con **Spring Boot**, **validaciones robustas**, **tests automatizados**, **documentación Swagger**, **deduplicación con hash**, y **cobertura de código >90%**.

---

##  Características principales

| Funcionalidad | Estado |
|---------------|--------|
| Detección de mutantes (horizontal, vertical, diagonal) | Implementado |
| Validación de entrada con Bean Validation | Mejorado |
| Deduplicación de ADN con hash único | Implementado |
| Tests unitarios y de integración | 32 tests verdes |
| Code coverage >90% | Con JaCoCo |
| Documentación Swagger | Con anotaciones |
| Manejo de excepciones global | Personalizado |
| API REST documentada y funcional | Swagger UI activo |
| Lombok para código limpio | Usado en entidades y DTOs |
| Respuestas HTTP correctas | 200, 403, 400 |

---

##  ¿Cómo usar este proyecto?

### 1. Clonar el repositorio
```bash
git clone https://github.com/abigailmunoz-glitch/mutant-detector.git
cd mutant-detector
```

### 2. Construir el proyecto
```bash
./gradlew build
```

### 3. Ejecutar tests
```bash
./gradlew test
```

### 4. Generar reporte de cobertura
```bash
./gradlew jacocoTestReport
# Ver: build/reports/jacoco/test/html/index.html
```

### 5. Ejecutar aplicación
```bash
./gradlew bootRun
# App: http://localhost:8080
# Swagger: http://localhost:8080/swagger-ui.html
```

---

## Comandos útiles

| Comando | Descripción |
|---------|-------------|
| `./gradlew build` | Compilar proyecto |
| `./gradlew test` | Ejecutar todos los tests |
| `./gradlew jacocoTestReport` | Generar cobertura |
| `./gradlew bootRun` | Levantar app local |
| `./gradlew clean build` | Limpiar y recompilar |
| `./gradlew test --tests MutantDetectorTest` | Tests unitarios |
| `./gradlew test --tests MutantControllerTest` | Tests integración |
| `./gradlew test jacocoTestReport --no-daemon` | Tests + cobertura |
| `./gradlew bootJar` | Generar JAR ejecutable |

---

## Endpoints de la API

### Detectar mutante
**POST** `/api/v1/mutant`  
**Body:**
```json
{
  "dna": ["ATGCGA","CAGTGC","TTATGT","AGAAGG","CCCCTA","TCACTG"]
}
```
**Respuestas:**
- `200 OK` → es mutante
- `403 Forbidden` → es humano
- `400 Bad Request` → ADN inválido

###  Estadísticas
**GET** `/api/v1/stats`  
**Respuesta:**
```json
{
  "count_mutant_dna": 40,
  "count_human_dna": 100,
  "ratio": 0.4
}
```

---

## Swagger UI

Documentación interactiva:  
👉 [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

---

## Algoritmo

- Recorrido único de la matriz
- Terminación anticipada al encontrar >1 secuencia
- Detección en horizontal, vertical y ambas diagonales
- Validación de entrada robusta con Bean Validation
- Deduplicación con hash único por ADN

---

## Tests

- **32 tests totales**
- **12 tests de integración**
- **20+ tests unitarios**
- **Code coverage >90%**
- **JaCoCo activo**

---

## 🧑‍💻 Autor

**Abigail Muñoz**  
[GitHub](https://github.com/abigailmunoz-glitch)  


¿O **lo subís directamente a GitHub** desde la web?  
¡**Con esto cerrás el examen con Excelencia**! 🎉
