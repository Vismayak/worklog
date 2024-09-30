---
description: Blog updates for my work at Illinois NRS Dashboard
icon: display-code
---

# Illinois NRS Dashboard

## Streamlit Notes (2024-09-29)

**Streamlit** is a Python library that allows you to create web applications with Python code. It is a great tool for creating dashboards and visualizations.

Install with pip:

```bash
pip install streamlit
```

You can run a Streamlit app with the following command:

```bash
streamlit run app.py
```

or 

```bash
python -m streamlit run app.py
```

During development, similar to Javascript development, the changes are automatically reflected in the browser.

Streamlit is a reactive framework. When the user interacts with the app, the app is re-run from top to bottom. This is different from traditional web frameworks where the server sends the data to the client. Also when you modify the code, the app is re-run.



To display data, we can use either magic commands or the `st.write()` function. The `st.write()` function is a generic function that can display any data type. 

It has support for dataframes, charts and maps. It also has widgets for user input.
The thing is there is a lack of flexibility in the layout but it is amazing for quick charts and stuff. I think it is a great tool for Clowder where we can provide support for data from clowder right in the dashboard. It has features like caching to perform when loading data.

![alt text](image.png)


It has support for custom componenets, so though there is no integration with Openlayers, we can create a custom component to display Openlayers maps. 

It also has a testing framework built in.

Here is an [App model summary](https://docs.streamlit.io/get-started/fundamentals/summary)

Overall the dashboard is very easy to use and is a great tool for creating dashboards and visualizations. It is quick and easy to use.

I was able to create the following dashboard through this [tutorial](https://docs.streamlit.io/get-started/tutorials/create-an-app) with just 36 lines of code. It includes loading data, optionally displaying data, creating a chart and a map. The data is loaded from an online source and cached for performance.



![alt text](image-1.png)