# Audioguía geolocalizada — prototipo v1

## Probar

Publicar estos archivos en GitHub Pages, o ejecutar en la carpeta `python3 -m http.server 8000` y abrir `http://localhost:8000`. El mapa necesita internet para Leaflet, los mosaicos OpenStreetMap y JSZip. GPS y micrófono requieren HTTPS o localhost.

## Administración

- **Spots:** crear, seleccionar, tocar el mapa para ubicar, configurar radio, texto, imagen, cargar o grabar audio.
- **Recorridos:** crear, dibujar vértices en el mapa, asignar y ordenar spots compartidos.
- **Cursos:** crear y asignar recorridos.
- **Simulador GPS:** elegir recorrido y tocar el mapa; salir a más de 1,5 veces el radio y volver para reactivar.
- **Publicar:** descargar ZIP de sitio estático que incorpora datos y archivos multimedia, subir su contenido al repositorio GitHub Pages.

## Limitaciones importantes

1. El editor guarda cambios en el almacenamiento local del navegador; **no sincroniza** entre dispositivos. Exportar JSON como respaldo. Los archivos multimedia grandes pueden superar la cuota de localStorage. Para producción, reemplazarlo por IndexedDB.
2. Los enlaces por curso son filtros, no controles de acceso: todo el contenido publicado es público.
3. En iOS/Android la reproducción automática y el GPS en segundo plano no están garantizados. Se incluye modo manual.
4. El GPS tiene imprecisión; radios pequeños pueden dispararse irregularmente.
5. Las dependencias JS se cargan de CDN y los mosaicos OSM necesitan conexión. El prototipo no tiene modo offline.
6. Los cambios locales del administrador no se publican automáticamente: hay que volver a exportar y subir los archivos.
7. Para editar desde la publicación de GitHub Pages, hacerlo en un navegador de confianza. El panel no está protegido con contraseña.
8. Para pruebas completas de grabación, geolocalización y publicación, usar un celular real.

## Licencias y servicios

Leaflet (BSD-2-Clause), JSZip (MIT), OpenStreetMap (ODbL, atribución visible). Respetar la política de uso de los mosaicos públicos de OSM.
