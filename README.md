# ADR-01: “Recordatorio”

| Campo  | Valor |
|--------|--------|
| Autor  | Leonardo Torres |
| Fecha  | 15/05/2026 |
| Estado | `Aceptado` |

---

## Contexto

El proyecto **Recordatorio** busca resolver el problema de la mala organización del tiempo en personas que necesitan administrar actividades, tareas y compromisos con fechas límite.

El sistema está pensado inicialmente para uso personal, pero puede aplicarse a estudiantes, trabajadores o cualquier persona con horarios estructurados que requieran avisos constantes.

El objetivo principal es permitir que el usuario reciba **notificaciones frecuentes**, recordatorios de tareas por vencer y avisos sobre actividades programadas.

El sistema maneja entidades como:

- **Tiempo**
- **Personas**
- **Tareas**
- **Actividades**

Las restricciones principales incluyen:

- Tiempo limitado para el desarrollo.
- Conocimientos previos adquiridos en clase.
- Necesidad de una solución simple, mantenible y escalable.
- Uso de tecnologías conocidas para asegurar estabilidad.

---

## Decisión

Se decidió implementar el sistema utilizando una **arquitectura basada en entidades y servicios**, donde cada módulo (tareas, actividades, tiempos, usuarios) se gestiona mediante componentes separados y bien definidos.

### ¿Por qué?

Porque este enfoque permite:

- Separar la lógica de negocio de la lógica de presentación.
- Facilitar la escalabilidad del sistema cuando se agreguen nuevas funciones como notificaciones automáticas, historial de actividades o sincronización con calendarios.
- Mantener el código más ordenado, entendible y fácil de modificar.
- Reutilizar componentes como servicios de tiempo o manejo de tareas en diferentes partes del sistema.

### Alternativas consideradas

| Alternativa | Por qué la descarté |
|-------------|---------------------|
| Arquitectura monolítica sin separación por capas | Se vuelve difícil de mantener y escalar cuando aumentan las funcionalidades. |
| Uso de un framework complejo (como microservicios) | Excesivo para el tamaño actual del proyecto y requiere más tiempo y recursos. |
| Implementación sin entidades claras (todo en un solo módulo) | Genera desorden, dificulta pruebas y complica agregar notificaciones o nuevas funciones. |

---

## Consecuencias

###  Lo que gano

- **Consecuencia técnica:**  
  El sistema se vuelve más fácil de mantener y extender. Agregar nuevas funciones como recordatorios inteligentes o integración con calendarios será más sencillo gracias a la separación por entidades y servicios.

- **Consecuencia sobre el proceso o el equipo:**  
  La estructura clara permite que cualquier colaborador entienda rápidamente el proyecto y pueda trabajar en módulos específicos sin afectar el resto del sistema.

---

###  Lo que sacrifico o asumo

- **Limitación técnica:**  
  La arquitectura requiere definir correctamente las entidades desde el inicio. Si cambian mucho en el futuro, habrá que refactorizar varias partes del sistema.


## Diagrama

Un boceto de cómo se estructura tu sistema (draw.io, Mermaid o a mano escaneado):


