import streamlit as st
import random

# Función para generar un ejercicio de cinemática
def generate_exercise():
    # Datos para el ejercicio
    initial_velocity = random.randint(10, 30)  # Velocidad inicial en m/s
    time = random.randint(1, 10)  # Tiempo en segundos
    acceleration = random.randint(1, 5)  # Aceleración en m/s²
    
    # Calcular la distancia usando la fórmula: d = v0 * t + 0.5 * a * t²
    distance = initial_velocity * time + 0.5 * acceleration * time ** 2
    return initial_velocity, time, acceleration, distance

# Generar un nuevo ejercicio
initial_velocity, time, acceleration, correct_answer = generate_exercise()

# Configuración de la aplicación
st.title("Generador de Ejercicios de Cinemática")
st.write("Resuelve el siguiente ejercicio:")

# Mostrar el ejercicio
st.write(f"Un objeto se mueve con una velocidad inicial de **{initial_velocity} m/s**.")
st.write(f"Después de **{time} segundos** y con una aceleración de **{acceleration} m/s²**, ¿cuál es la distancia recorrida?")
st.write("Introduce tu respuesta en metros:")

# Entrada de respuesta del usuario
user_answer = st.number_input("Respuesta:", min_value=0.0)

# Botón para verificar la respuesta
if st.button("Verificar respuesta"):
    if user_answer == correct_answer:
        st.success("¡Correcto! La distancia recorrida es efectivamente de {:.2f} metros.".format(correct_answer))
    else:
        st.error("Incorrecto. La distancia recorrida es de {:.2f} metros.".format(correct_answer))

# Permitir generar un nuevo ejercicio
if st.button("Generar nuevo ejercicio"):
    st.experimental_rerun()
