# Activar archivos privados en Rodme Garage

1. Abrí Firebase Console > proyecto rodme-garage > Storage.
2. Activá Cloud Storage si aún no está habilitado (puede requerir configurar facturación según el proyecto y su región).
3. En Storage > Rules, copiá las reglas de `storage.rules` del repositorio y pulsá **Publish**.
4. Confirmá que Authentication y Firestore estén habilitados y que `firestore.rules` se hayan desplegado.
5. Iniciá sesión en Rodme Garage con tu cuenta. Entrá a **Archivos**, seleccioná el vehículo, subí una imagen de prueba y verificá que puedas abrirla y eliminarla.
6. Comprobá en otro dispositivo usando la misma cuenta. No habilités permisos públicos ni de lectura anónima.

**Importante:** Guardar reglas en GitHub no las despliega en Firebase. La aplicación no debe afirmar que un archivo quedó almacenado hasta recibir confirmación de Storage. Para compartir vehículos con familiares de manera segura se requiere un diseño de ACL y reglas por propietario e invitado, con pruebas de aislamiento entre cuentas. El sistema actual permanece privado.

**Conflictos:** Si aparece un conflicto entre dispositivos, entrá en Respaldos y utilizá "Guardar copia y recuperar versión de Firebase". La copia descargada conserva cambios locales para recuperación manual. No fusiona ediciones automáticamente.

**Respaldos:** Las copias automáticas del navegador no sustituyen una copia de seguridad programada e independiente de Firebase.
