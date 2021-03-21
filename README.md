# 09GridAutoFillAuto-fit
09 grid auto-fit y auto fill ejemplos

```javascript
.servicios {
    border: 3px solid black;
    height: 300px;
    display:grid;
    grid-template-columns: repeat(3, 1fr);
/* desventaja no se ajusta a la pantalla */
    grid-template-columns: repeat(5,200px);
/* mantiene los 200px. Pero al disminuir la pantalla,el ancho las cajas se ajusten hacia abajo */
/* evitando el scroll horizontal */
/* El problema es que deja un espacio en blanco en el lado derecho */
    grid-template-columns: repeat(auto-fill, 200px);
/* el espacio en blanco se puede cubrir añadiendo un minmax */
/* se ajustará al tamañano de la pantalla con mayor eficacia */
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
/* la desventaja que crea espacio vacios en la pantalla sin contenido */
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
/*auto-fit quita los espacios vacios y se ajusta a la pantalla  */
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
}
```
