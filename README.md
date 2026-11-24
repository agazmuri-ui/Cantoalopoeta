# Endecimados

Taller interactivo para aprender a escribir **décimas** (espinelas), desde la tradición chilena del canto a lo poeta. Está pensado para estudiantes desde los 10 años y para adultos.

## Estaciones
1. **¿Qué es la décima?** Su forma (10 versos octosílabos, rima ABBAACCDDC) y un quiz.
2. **La décima viajera.** Historia, el canto a lo poeta en Chile y un mapa interactivo de América Latina con un desafío.
3. **Taller de sílabas.** Conteo métrico con sinalefa y ley del acento final, más un laboratorio de versos.
4. **Cazador de rimas.** Rima consonante y asonante, un juego y un banco de rimas.
5. **Escribe tu décima.** Editor guiado que cuenta sílabas y revisa rimas en vivo. Tiene modo pie forzado.
6. **Antología.** Décimas clásicas y las décimas propias, guardadas en el navegador.

## Uso
App publicada: https://agazmuri-ui.github.io/Cantoalopoeta/

Para entrar hay que iniciar sesión con una cuenta de Google. El avance (estrellas, borrador y antología) se guarda en la nube, en Firebase Firestore, en el documento `users/{uid}`. Así cada persona recupera su trabajo en cualquier computador.

Si abres `index.html` con doble clic no se puede iniciar sesión. La app tiene que abrirse desde un servidor web.

## Configurar Firebase (una sola vez)
1. Crea un proyecto en https://console.firebase.google.com (puedes desactivar Analytics).
2. **Authentication → Comenzar → Método de acceso → Google →** Habilitar. Elige un correo de soporte.
3. **Authentication → Configuración → Dominios autorizados →** agrega `agazmuri-ui.github.io`.
4. **Firestore Database → Crear base de datos.** Elige una ubicación (por ejemplo `southamerica-east1`) e inicia en modo producción.
5. **Firestore → Reglas →** pega el contenido de `firestore.rules` y publica.
6. **Configuración del proyecto → Tus apps → Web (`</>`) →** registra la app y copia el objeto `firebaseConfig` en `firebase-config.js`.
