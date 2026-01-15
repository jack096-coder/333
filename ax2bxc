import streamlit as st
import numpy as np
import matplotlib.pyplot as plt

# 設定網頁標題
st.title("quadratic-function-plotter 🚀")
st.subheader("繪製一元二次函數： y = ax² + bx + c")

# 讓使用者輸入係數 a, b, c
st.sidebar.header("請輸入函數係數：")
a = st.sidebar.number_input("係數 a", value=1.0, step=0.1)
b = st.sidebar.number_input("係數 b", value=0.0, step=0.1)
c = st.sidebar.number_input("係數 c", value=0.0, step=0.1)

# 提示使用者係數 a 不能為 0
if a == 0:
    st.warning("係數 'a' 不能為 0，否則這將是一個一次函數。")
    st.stop() # 停止程式執行，直到 a 不為 0

# 生成 x 軸數據點
x = np.linspace(-10, 10, 400) # 從 -10 到 10，生成 400 個點

# 計算 y 軸數據點
y = a * x**2 + b * x + c

# 繪製圖形
fig, ax = plt.subplots()
ax.plot(x, y, label=f'y = {a}x² + {b}x + {c}')

# 設定圖形標題和軸標籤
ax.set_title("一元二次函數圖形")
ax.set_xlabel("x 軸")
ax.set_ylabel("y 軸")
ax.grid(True)
ax.axhline(0, color='black', linewidth=0.5) # 繪製 x 軸
ax.axvline(0, color='black', linewidth=0.5) # 繪製 y 軸
ax.legend()

# 顯示圖形
st.pyplot(fig)

# 顯示函數的頂點 (Vertex)
if a != 0:
    vertex_x = -b / (2 * a)
    vertex_y = a * (vertex_x**2) + b * vertex_x + c
    st.write(f"函數的頂點 (Vertex) 位於：({vertex_x:.2f}, {vertex_y:.2f})")

st.markdown("---")
st.markdown("由 Streamlit 製作")
