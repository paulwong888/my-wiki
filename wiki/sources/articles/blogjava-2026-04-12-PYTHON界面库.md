---
title: PYTHON界面库
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2024/08/12/451478.html
author: paulwong
tags: ['blogjava']
---

# PYTHON界面库

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/08/12/451478.html  
**发布时间**: 2026-04-12

## 摘要

# PYTHON界面库

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/08/12/451478.html
**发布时间**: 2026-04-12

PYTHON界面库
python服务器脚本，生成html，无需写js,css，适合AI项目
https://cheat-sheet.streamlit.app



生成文字的代码：
st.text('Fixed width text')
st.markdown('_Markdown_') # see #*
st.caption('Balloons. Hundreds of them')
st.latex(r''' e^{i\\pi} + 1 = 0 ''')
st.write('Most objects') # df, err, func, keras!
st.write(['st', 'is <', 3]) # see *
st.title('My title')
st.header('My header')
st.subheader('My sub')
st.cod...

## 原文内容

# PYTHON界面库

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/08/12/451478.html
**发布时间**: 2026-04-12

PYTHON界面库
python服务器脚本，生成html，无需写js,css，适合AI项目
https://cheat-sheet.streamlit.app



生成文字的代码：
st.text('Fixed width text')
st.markdown('_Markdown_') # see #*
st.caption('Balloons. Hundreds of them')
st.latex(r''' e^{i\\pi} + 1 = 0 ''')
st.write('Most objects') # df, err, func, keras!
st.write(['st', 'is <', 3]) # see *
st.title('My title')
st.header('My header')
st.subheader('My sub')
st.code('for i in range(8): foo()')

# * optional kwarg unsafe_allow_html = True


生成form控件：
st.button('Hit me')
st.data_editor('Edit data', data)
st.checkbox('Check me out')
st.radio('Pick one:', ['nose','ear'])
st.selectbox('Select', [1,2,3])
st.multiselect('Multiselect', [1,2,3])
st.slider('Slide me', min_value=0, max_value=10)
st.select_slider('Slide to select', options=[1,'2'])
st.text_input('Enter some text')
st.number_input('Enter a number')
st.text_area('Area for textual entry')
st.date_input('Date input')
st.time_input('Time entry')
st.file_uploader('File uploader')
st.download_button('On the dl', data)
st.camera_input(\

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
