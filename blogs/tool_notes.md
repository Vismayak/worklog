---
description: Notes on tools and technologies
icon: display-code
---

# Tool Notes


## [Gatsby](https://www.gatsbyjs.com/)

Gatsby is a React-based open source framework for creating websites. I think there is an use case for the Illinos NRS project because it is a static site generator with options to pull data from markdon and use something called MDX. 

Follow the [tutorial](https://www.gatsbyjs.com/docs/tutorial/getting-started/). 

Key points from the tutorial:

**Part 2** 
- Gatsby automatically creates pages for React components that are the default export of files in the src/pages directory.

- If a user tries to visit the URL for a page that doesn’t actually exist, Gatsby will use the src/pages/404.js page component to display an error instead.

- Add a page title to your page. Gatsby lets you define a title and other document metadata with the Gatsby Head API. You have to export a component called Head from your page template to apply the metadata. Adding such metadata helps search engines like Google to better understand your site. For this tutorial you’ll only be adding titles to pages but you can also later add other metadata.

- Encompass the repeated parts of your site in a layout component. You can create a layout component that wraps around your page components to encompass the repeated parts of your site. This makes it easier to maintain your site and ensures that all pages have a consistent look and feel.
- Gatsby isn’t opinionated about what styling approach you want to use, but it works with CSS Modules by default.

**Part 3**

- In Gatsby terms, a plugin is a separate npm package that you install to add extra features to your site.

To add a plugin to your site, you’ll use the following process:

1. Install the plugin by running npm install or yarn add.
2. Configure the plugin to your gatsby-config.js file.

*The gatsby-config.js file is a special file that Gatsby recognizes automatically. It’s where you add plugins and other site configuration.*



## [uv](https://github.com/astral-sh/uv) 

An extremely fast Python package and project manager, written in Rust.

**Installation**

```bash
# On Linux.
curl -LsSf https://astral.sh/uv/install.sh | sh

# On mac.
brew install uv
uv 
```

**Creating a virtual environment**

```bash
uv venv my_env
```

**Activating a virtual environment**

```bash
source my_env/bin/activate
```

**Deactivating a virtual environment**

```bash
deactivate
```

**Installing a package**

```bash
uv pip install numpy
```


## Streamlit

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

![alt text](assets/images/tool_notes/image.png)

It has support for custom componenets, so though there is no integration with Openlayers, we can create a custom component to display Openlayers maps. 

It also has a testing framework built in.

Here is an [App model summary](https://docs.streamlit.io/get-started/fundamentals/summary)

Overall the dashboard is very easy to use and is a great tool for creating dashboards and visualizations. It is quick and easy to use.

I was able to create the following dashboard through this [tutorial](https://docs.streamlit.io/get-started/tutorials/create-an-app) with just 36 lines of code. It includes loading data, optionally displaying data, creating a chart and a map. The data is loaded from an online source and cached for performance.


![alt text](assets/images/tool_notes/image-1.png)