VocaACC
App Android de Comunicación Aumentativa y Alternativa (ACC) para terapia del habla. Desarrollada con Kotlin y Java. Basada en el diseño de Figma del equipo #1.
Pantallas
1.
Principal: Lector de tarjetas, botón Reproducir, "Usados recientemente" y barra inferior (Teclado, Emergencia, Categorías).
2.
Emergencia: Baño, Ayuda, Malestar y Dolor. Un toque y la app lo dice en voz alta.
3.
Categorías: Personalizado, Comida, Emociones, Necesidades, Actividades, Ocupaciones y Personas.
4.
Teclado: escribir una frase y decirla, o guardarla como tarjeta.
Innovación
•
Tablero adaptativo: "Usados recientemente" se reordena según la hora del día (mañana / tarde / noche).
•
Animaciones configurables: chip ✦ arriba a la derecha → Completa, Suave o Apagada.
Mejoras recientes
•
Voz más confiable: avisa si el teléfono no tiene voz en español, evita que el botón se quede "Hablando" por errores o frases que se pisan, y los cambios de estado se hacen en el hilo principal.
•
Botón Detener: tocar Reproducir mientras habla corta la voz.
•
Accesibilidad: la primera vez, si el teléfono tiene las animaciones del sistema apagadas, la app arranca en modo Apagada.
•
Teclado: se abre solo, tiene botón Borrar, mayúscula automática y avisa si la tarjeta se guardó o ya existía.
•
Los textos largos en las tarjetas se cortan con "…" en vez de desbordarse.
Cómo abrirlo
1.
Android Studio (Koala o más nuevo) → File > Open → elige la carpeta VocaACC.
2.
Espera el Gradle Sync (necesita internet la primera vez). Si pide actualizar AGP/Gradle, acepta.
3.
Elige un emulador (API 26+) o un teléfono y presiona ▶ Run.
4.
Para escuchar la voz: el emulador/teléfono necesita voz en español instalada (Ajustes > Salida de texto a voz).
Estructura
app/src/main/java/com/equipo1/vocaacc/
├── MainActivity.kt          punto de entrada
├── data/                    Modelos.kt (Picto, Categoria), AnimPrefs.kt (modos de animación), Prefs.kt
├── viewmodel/TableroVM.kt   lógica: oración, voz, usos por franja del día
└── ui/                      Componentes.kt, Principal/Emergencia/Categorias/CategoriaDetalle/Teclado, Navegacion.kt
Control de versiones (Git + GitHub)
git init
git add .
git commit -m "feat: proyecto inicial VocaACC"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/VocaACC.git
git push -u origin main
git checkout -b develop
git checkout -b feature/animaciones
