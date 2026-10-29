Win11Dark - tema oscuro para IceWM (estilo Windows 11)

INSTALACION RAPIDA (recomendada, instala el tema Y el menu de apps):
  mkdir -p ~/.icewm/themes
  unzip Win11Dark.zip -d ~/.icewm/themes/
  sh ~/.icewm/themes/Win11Dark/extras/instalar.sh
  icewm --restart

INSTALACION MANUAL (solo el tema):
  unzip Win11Dark.zip -d ~/.icewm/themes/
  Poner en ~/.icewm/theme:   Theme="Win11Dark/default.theme"
  icewm --restart

IMPORTANTE - EL MENU NO ES PARTE DEL TEMA:
  Las aplicaciones del menu de inicio las define el archivo ~/.icewm/menu
  (no el tema). Por eso un tema solo cambia colores y botones; el menu con tus
  apps lo arma extras/instalar.sh. Si ya tenias un ~/.icewm/menu propio,
  el instalador te deja una copia como ~/.icewm/menu.bak.<numero>.

  Si el menu "Aplicaciones" sale vacio, probar:
     sh ~/.icewm/menu-apps.sh | head
  Si no muestra nada, no hay archivos .desktop en /usr/share/applications.

OTROS AJUSTES:
  - Fondo de pantalla: DesktopBackgroundImage="/ruta/imagen.jpg" en
    ~/.icewm/preferences (tiene prioridad sobre el tema).
  - Color de acento: reemplazar rgb:00/67/C0 en default.theme.
  - Fuente: cambiar "sans-serif" por Inter, Noto Sans, etc. en las lineas ...FontNameXft.
