

# =========================
# ☠️ HADES — ALL-IN-ONE
# =========================

import streamlit as st
import yfinance as yf
import pandas as pd
import numpy as np
from sklearn.ensemble import RandomForestClassifier
from datetime import datetime, timedelta

# =========================
# 🧾 PAGE CONFIG
# =========================
st.set_page_config(
    page_title="HADES AI",
    page_icon="logo.png",
    layout="wide"
)

# =========================
# ☠️ CORE SETTINGS
# =========================
INITIAL_CAPITAL = 7000
COOLDOWN_DAYS = 3

HADES = {
    "drawdown_limit": 0.10,
    "confidence_threshold": 0.65
}

# =========================
# 🖼️ HEADER
# =========================
st.markdown("<h1 style='text-align:center;'>☠️ HADES</h1>", unsafe_allow_html=True)
st.image("logo.png", use_container_width=True)
st.caption("Trade | Analyze | Dominate")

# =========================
# ⏳ WEEK TIMER
# =========================
if "start_time" not in st.session_state:
    st.session_state.start_time = datetime.now()

end_time = st.session_state.start_time + timedelta(days=7)
remaining = end_time - datetime.now()

st.write("⏳ Weekly Timer Remaining:", remaining)

if remaining.total_seconds() <= 0:
    st.warning("New week started")
    st.session_state.start_time = datetime.now()

# =========================
# 💬 CHAT MEMORY
# =========================
if "messages" not in st.session_state:
    st.session_state.messages = []

# =========================
# ⚙️ SIDEBAR CONFIG
# =========================
st.sidebar.image("logo.png", use_container_width=True)
st.sidebar.header("Hades Config")

config = {
    "assets
jobs:
  awesome-lint:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
      with: 
        fetch-depth: 0
    - uses: actions/setup-node@v1
      with:
        node-version: '14.x'
    - run: npm install
    - run: npm test# Hedes
Trading a.i
