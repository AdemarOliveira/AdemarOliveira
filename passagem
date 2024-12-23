import streamlit as st

st.title("Controle de Passagem de Turno")

def registrar_passagem(turno):
    st.session_state.passagens.append(turno)

if 'passagens' not in st.session_state:
    st.session_state.passagens = []

with st.form(key='passagem_form'):
    turno = st.selectbox("Escolha o turno:", ["Manhã", "Tarde", "Noite"])
    submitted = st.form_submit_button("Registrar Passagem")
    if submitted:
        registrar_passagem(turno)
        st.success(f"Passagem do turno '{turno}' registrada com sucesso!")

st.write("Passagens registradas:")
for passagem in st.session_state.passagens:
    st.write(passagem)
