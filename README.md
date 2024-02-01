# Acortador
Acortador de links

import pyshorteners
import streamlit as st

def shorten_url(url):
    S =pyshorteners.Shortener()
    shorten_url = S.tinyurl.short(url)
    return shorten_url
st.set_page_config(page_title="AcortadorLink",page_icon="🔗", layout="centered")
st.image("images/www.png", use_column_width=True)
st.title("AcortadorLink")
url = st.text_input("Ingrese el link que quiera acortar...")
if st.button("Crear nuevo link"): 
    st.write("Link Acortado: ", shorten_url(url)) 
