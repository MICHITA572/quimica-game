# quimica-game
quimica elements study
import streamlit as st
import random

# Diccionario de elementos químicos
elementos = {
    "H": "Hidrógeno",
    "He": "Helio",
    "Li": "Litio",
    "Be": "Berilio",
    "B": "Boro",
    "C": "Carbono",
    "N": "Nitrógeno",
    "O": "Oxígeno",
    "F": "Flúor",
    "Ne": "Neón",
}

# Seleccionar un elemento aleatorio
simbolo, nombre_correcto = random.choice(list(elementos.items()))

st.title("Juego de Elementos Químicos 🧪")

st.write(f"¿Cuál es el nombre del elemento con el símbolo **{simbolo}**?")

# Entrada del usuario
respuesta_usuario = st.text_input("Escribe el nombre del elemento:")

if st.button("Verificar"):
    if respuesta_usuario.strip().lower() == nombre_correcto.lower():
        st.success("✅ ¡Correcto!")
    else:
        st.error(f"❌ Incorrecto. La respuesta correcta es **{nombre_correcto}**.")

st.write("¡Inténtalo de nuevo recargando la página!")

