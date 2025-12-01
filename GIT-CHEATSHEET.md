# 🚀 Git Cheat Sheet - Mondriart

## Comandos Diarios

### Ver Estado
```bash
git status              # Ver archivos modificados
git log --oneline       # Ver historial de commits
git diff                # Ver cambios sin stagear
```

### Hacer Cambios
```bash
git add .               # Agregar todos los cambios
git commit -m "mensaje" # Hacer commit
git push origin main    # Subir a GitHub
```

### Ramas
```bash
git branch                      # Ver ramas
git checkout -b feature/nombre  # Crear y cambiar a rama
git checkout main               # Volver a main
git merge feature/nombre        # Fusionar rama en main
git branch -d feature/nombre    # Eliminar rama local
```

### Sincronizar
```bash
git pull origin main    # Traer cambios de GitHub
git fetch              # Ver cambios sin aplicar
```

### Deshacer
```bash
git checkout -- archivo     # Descartar cambios en archivo
git reset --soft HEAD~1     # Deshacer último commit (mantener cambios)
git reset --hard HEAD~1     # Deshacer último commit (borrar cambios)
```

---

## 🌿 Workflow Recomendado

1. **Crear rama para nueva funcionalidad:**
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```

2. **Hacer cambios y commits:**
   ```bash
   # Editar archivos...
   git add .
   git commit -m "Agregar nueva funcionalidad"
   ```

3. **Volver a main y fusionar:**
   ```bash
   git checkout main
   git merge feature/nueva-funcionalidad
   ```

4. **Subir a GitHub:**
   ```bash
   git push origin main
   ```

5. **Limpiar rama:**
   ```bash
   git branch -d feature/nueva-funcionalidad
   ```

---

## ⚠️ Comandos Peligrosos (Usar con Cuidado)

```bash
git push --force origin main    # Forzar push (puede sobrescribir cambios)
git reset --hard                # Borra cambios locales permanentemente
git clean -fd                   # Elimina archivos no trackeados
```

---

## 🔗 Enlaces Útiles

- Repositorio: https://github.com/jpablokhipu/mondriart
- Sitio: https://jpablokhipu.github.io/mondriart/
- GitHub Pages Settings: https://github.com/jpablokhipu/mondriart/settings/pages

---

## 📝 Convenciones de Mensajes de Commit

```
feat: Nueva funcionalidad
fix: Corrección de bug
improve: Mejora de funcionalidad existente
refactor: Refactorización de código
docs: Cambios en documentación
style: Cambios de estilo/formato
test: Agregar o modificar tests
```

**Ejemplos:**
```bash
git commit -m "feat: agregar pregunta condicional #7"
git commit -m "fix: corregir detección de categorías"
git commit -m "improve: optimizar ejemplos de prompts"
```
