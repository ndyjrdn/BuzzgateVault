# Scene Plan: {{title}}

## 🧠 Purpose
Brief description of the scene’s goal or vibe.

## 🛠️ Trigger Logic
- Trigger type: `motion` / `time` / `manual` / `sensor`
- Entity: `sensor.bedroom_motion`
- Conditions:
  - Time window: `07:00–09:00`
  - State: `on`

## 💡 Actions
```yaml
- service: light.turn_on
  target:
    entity_id: light.bedroom_main
  data:
    brightness: 180
    color_name: "warm white"
