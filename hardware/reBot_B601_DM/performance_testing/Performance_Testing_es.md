# 🧪 Referencia de Pruebas de Rendimiento Físico reBot-DevArm

<p align="center">
  <img src="./images/v1.0.png" alt="reBot-DevArm Banner">
</p>

<p align="center">
  <strong>
    <a href="./Performance_Testing_zh.md">简体中文</a> &nbsp;|&nbsp;
    <a href="./Performance_Testing.md">English</a> &nbsp;|&nbsp;
    <a href="./Performance_Testing_JP.md">日本語</a>&nbsp;|&nbsp;
    <a href="./Performance_Testing_Fr.md">français</a>&nbsp;|&nbsp;
    <a href="./Performance_Testing_es.md">Español</a>
  </strong>
</p>

> [!NOTE]
> Este documento proporciona datos de referencia de pruebas de rendimiento para el brazo robótico reBot Arm B601-DM en condiciones de trabajo normales y extremas.

> [!WARNING]
> **Aviso de Diferencia de Versión**: Esta prueba se basa en el reBot Arm B601-DM equipado con **motores Damiao versión V4**. **Las versiones V3 y anteriores de los motores tienen diferencias de rendimiento**. Los datos de prueba son solo para referencia; el rendimiento real debe verificarse mediante pruebas.

---

## 💡 Resumen Rápido

**Motivo de Terminación de las Pruebas**: Todas las pruebas se terminaron debido a la **protección por sobrecalentamiento del motor 2 (articulación del brazo superior)**, no por fallo de la estructura mecánica.

**Prueba de Movimiento Dinámico** (Duración de un ciclo de movimiento: 5s estándar, movimiento de vaivén):

| Rango de Alcance | Carga | Duración | Motivo de Terminación |
|----------|------|----------|----------|
| 5%~70% del Alcance Nominal | 1.5 kg | > 2 h | Temperatura del motor 2 alcanzó 90℃ |
| 5%~70% del Alcance Nominal | 2.5 kg | 40 min | Protección por sobrecalentamiento del motor 2 |
| 5%~100% del Alcance Nominal | 1.5 kg | 45 min | Protección por sobrecalentamiento del motor 2 |

**Prueba de Mantenimiento Estático**:

| Posición de Alcance | Carga | Duración | Motivo de Terminación |
|----------|------|----------|----------|
| 70% del Alcance Nominal | 1.5 kg | 18 min | Protección por sobrecalentamiento del motor 2 |
| 100% del Alcance Nominal | 1.5 kg | 3 min | Protección por sobrecalentamiento del motor 2 |

> 👉 **Conclusión Clave**: La resistencia estructural del manipulador es suficiente. La terminación de las pruebas se debió a la **protección por sobrecalentamiento del motor 2**. La carga de trabajo recomendada es de **1.5 kg o menos**, el alcance de trabajo recomendado es **menor al 70%**, y se recomienda agregar medidas de refrigeración activa.

---

## 📋 Tabla de Contenidos

- [⚡ Prueba de Rendimiento en Condiciones Extremas](#-prueba-de-rendimiento-en-condiciones-extremas)
- [📈 Curva de Carga Oficial](#-curva-de-carga-oficial)
- [📝 Conclusiones y Recomendaciones de las Pruebas](#-conclusiones-y-recomendaciones-de-las-pruebas)
- [🙋 Preguntas Frecuentes (FAQ)](#-preguntas-frecuentes-faq)
- [📅 Historial de Actualizaciones](#-historial-de-actualizaciones)
- [📞 Soporte Técnico](#-soporte-técnico)

---

## ⚡ Prueba de Rendimiento en Condiciones Extremas

### Condiciones de la Prueba

**Prueba de Movimiento Dinámico**:
- Duración de un ciclo de movimiento: 5 s
- Modo de movimiento: Movimiento de vaivén
- Rango de alcance de prueba: 5%~70% / 5%~100% del alcance nominal

**Prueba de Mantenimiento Estático**:
- Postura de prueba: Mantenimiento de carga en postura estática
- Alcance de prueba: 70% / 100% del alcance nominal

### Resultados de las Pruebas

#### 1. Prueba de Movimiento Dinámico

| Posición de Prueba | Carga (kg) | Duración Máxima | Motivo de Terminación |
|----------|-----------|--------------|----------|
| Alcance 5%~70% | 1.5 | > 2 h | Protección por sobrecalentamiento del motor 2 |
| Alcance 5%~70% | 2.5 | 40 min | Protección por sobrecalentamiento del motor 2 |
| Alcance 5%~100% | 1.5 | 45 min | Protección por sobrecalentamiento del motor 2 |

#### 2. Prueba de Mantenimiento Estático

| Posición de Prueba | Carga (kg) | Duración Máxima | Motivo de Terminación |
|----------|-----------|--------------|----------|
| Alcance 70% | 1.5 | 18 min | Protección por sobrecalentamiento del motor 2 |
| Alcance 100% | 1.5 | 3 min | Protección por sobrecalentamiento del motor 2 |

---

## 📈 Curva de Carga Oficial

![Curva de Carga 12Nm](./images/12Nm.png)

<p align="center">Curva de Carga del Motor Serie Damiao 43 Versión 12Nm</p>

---

## 📝 Conclusiones y Recomendaciones de las Pruebas

### Recomendaciones de Uso

1. **Condiciones de Trabajo Recomendadas**
   - Carga: < 1.5 kg
   - Radio de trabajo: < 70% del alcance (450 mm)
   - Velocidad de movimiento: < 70% de la velocidad máxima
   - Temperatura ambiente: 15 °C ~ 35 °C

2. **Recomendaciones de Refrigeración**
   - Cuando se trabaje bajo carga elevada durante períodos prolongados, se recomienda agregar refrigeración activa
   - Después de 2 horas de trabajo continuo, se recomienda un descanso de 10~15 minutos
   - Evite la luz solar directa y el uso en espacios cerrados

---

## 🙋 Preguntas Frecuentes (FAQ)

<details>
<summary><b>P1: ¿El rendimiento del manipulador disminuye en ambientes de alta temperatura?</b></summary>

Sí. Cuando la temperatura ambiente supera los 35 °C o la temperatura del motor supera los 75 °C, se recomienda reducir la carga y la velocidad de movimiento para garantizar la precisión y la vida útil. No se recomienda el uso continuo en altas temperaturas.

</details>

<details>
<summary><b>P2: ¿Los datos de prueba son aplicables a todas las versiones?</b></summary>

Esta prueba se basa en el reBot Arm B601-DM equipado con **motores Damiao versión V4**. **Las versiones V3 y anteriores de los motores tienen diferencias de rendimiento**, por lo que los datos de prueba son solo para referencia.

</details>

---

## 📅 Historial de Actualizaciones

| Versión | Fecha | Contenido de la Actualización | Autor |
|------|------|----------|------|
| v1.0 | 2026.04.01 | Versión inicial, publicación de datos básicos de pruebas de rendimiento | SeeedStudio AI Robotics Team |

---

## 📞 Soporte Técnico

Si tiene alguna pregunta relacionada con las pruebas de rendimiento, no dude en contactarnos:

- **Soporte Técnico**: yaohui.zhu@seeed.cc
- **Discord**: [Unirse a la Comunidad](https://discord.gg/AbGuqJhDpQ)
- **Wiki**: [Ver Base de Conocimientos](https://wiki.seeedstudio.com/robotics_page/)

---

<p align="center">
  <strong>🤖 reBot-DevArm - Manipulador de Código Abierto para Cada Desarrollador</strong>
</p>
