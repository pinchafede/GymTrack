# GymTrack

**PWA de seguimiento de entrenamiento** — registrá tus sesiones de gym, deportes, suplementos y progreso físico desde el celular sin instalar nada.

🔗 **[Abrir la app](https://pinchafede.github.io/GymTrack/)**

---

## ¿Qué es?

GymTrack es una Progressive Web App (PWA) construida en HTML/CSS/JS puro. Funciona en el navegador del celular y se puede instalar en la pantalla de inicio como si fuera una app nativa. No requiere cuenta, no tiene servidor, todos los datos se guardan en el dispositivo.

---

## Funcionalidades

### 🏋️ Entrenamiento
- Rutinas con múltiples días configurables (Espalda, Pecho, Piernas, etc.)
- **Múltiples rutinas** — creá Semana A / Semana B y cambiá con un toque
- Series con peso y reps precargados desde la última sesión
- Swipe derecho para completar una serie
- **Ejercicios por tiempo** — cronómetro integrado para planchas, puentes, etc.
- Timer de descanso entre series con **sonido en auriculares**
- **RPE post-ejercicio** — sheet que aparece al completar todas las series
- Calentamiento y vuelta a la calma con check de completado
- Ejercicio extra en vivo con opción de agregar a la rutina permanentemente
- Confirmación antes de salir si hay series completadas
- Resumen post-sesión con PRs, volumen, calorías y duración

### 📊 Progreso y estadísticas
- Heatmap de actividad de las últimas 13 semanas
- Gráfico de volumen por sesión con colores por día de rutina
- Evolución de peso por ejercicio
- Récords personales detectados automáticamente

### 🧠 Coach
- Análisis de RPE: detecta ejercicios al límite o con potencial sin explotar
- Análisis de notas: detecta patrones de cansancio o racha positiva
- **📈 Progresión automática**: sugiere subir el peso cuando completaste 3 sesiones consecutivas con el mismo peso
- Vista útil desde la primera sesión

### 💊 Suplementos
- Grupos por momento (mañana / pre / post / noche)
- Checks diarios con hora de toma
- Reset automático al cambiar de día
- Notificaciones push configurables por momento y horario

### ⚽ Deportes
- Registrá actividades deportivas (fútbol, básquet, etc.)
- Configurá tu rol, MET y día habitual
- Cálculo de calorías por actividad

### 👤 Perfil y cuerpo
- BMR (gasto energético basal) calculado con fórmula Mifflin-St Jeor
- Registro de peso corporal con gráfico de evolución
- **Fotos de progreso** protegidas con PIN de 4 dígitos
- Registro de peso + foto integrados en un solo paso

### 🗂 Historial
- Agrupado por fecha local (sin bugs de UTC)
- PRs marcados en cada sesión
- **Editar sesión guardada** — corregí pesos y reps sin borrar la sesión
- Compartir resumen como imagen (Web Share API)

### ☁️ Sincronización
- **Google Drive sync** automático al guardar sesión y al abrir la app
- Restaurar desde Drive en el onboarding — sin necesidad del archivo JSON
- Backup/restore manual en JSON desde Ajustes

---

## Stack técnico

| Capa | Tecnología |
|------|-----------|
| Frontend | HTML5 / CSS3 / JavaScript vanilla |
| Gráficos | Chart.js 4.4.1 |
| Tipografía | Bebas Neue + DM Sans (Google Fonts) |
| Almacenamiento | localStorage |
| Sync | Google Drive API v3 (scope: `drive.appdata`) |
| PWA | Service Worker (network-first), Web App Manifest |
| Audio | Web Audio API |
| Deploy | GitHub Pages |

**Paleta:** fondo `#0a0a0a` · acento `#d4f53c` (verde lima)

---

## Instalación como PWA

**Android (Chrome):**
1. Abrí https://pinchafede.github.io/GymTrack/
2. Menú (⋮) → "Agregar a pantalla de inicio"

**iOS (Safari):**
1. Abrí https://pinchafede.github.io/GymTrack/
2. Botón compartir → "Agregar a pantalla de inicio"

---

## Biblioteca de ejercicios

119 ejercicios con información completa en español:

| Grupo | Ejercicios |
|-------|-----------|
| Espalda | 10 |
| Pecho | 10 |
| Hombros | 8 |
| Bíceps | 7 |
| Tríceps | 7 |
| Piernas | 12 |
| Core | 14 |
| Cardio | 8 |
| **Calistenia** | **29** |

---

## Google Drive Sync

Para usar el sync necesitás ser agregado como usuario de prueba. Contactar a Federico Díaz para acceso.

---

## Desarrollo local

```bash
git clone https://github.com/pinchafede/GymTrack.git
cd GymTrack
python3 -m http.server 8080
```

Sin dependencias de Node ni build step.

---

## Changelog reciente

```
4.0.0 — Rutinas múltiples (crear, cambiar, eliminar)
3.9.7 — Coach mejorado, progresión automática sugerida
3.9.6 — Reordenar ejercicios, leyenda colores en stats
3.9.5 — Fix weekday nuevo día, duración en historial
3.9.4 — Día recomendado por semana, editar sesión, 💡 119 ejercicios
3.9.3 — Fix fechas UTC, duración sesión, info ejercicios calistenia
3.8.0 — Workout: RPE sheet, ejercicios por tiempo, sonido timer
3.7.4 — Fix Drive scope appDataFolder entre dispositivos
3.7.0 — Confirmación salir workout, timer preciso, hints primera sesión
3.6.0 — Rediseño perfil, fix overscroll, peso+foto integrados
3.4.0 — Google Drive sync automático
3.3.0 — Exportar sesión como imagen
3.2.0 — Fotos de progreso con PIN
3.0.0 — RPE por ejercicio + análisis en Coach
```

---

## Roadmap

- [ ] Migración a Capacitor (APK nativa)
- [ ] Publicación en Google Play Store
- [ ] Sonido nativo en iOS con teléfono bloqueado
- [ ] Cámara nativa para fotos de progreso

---

*Uso personal. No redistribuir sin autorización.*
