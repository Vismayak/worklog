---
description: Notes on tools and technologies
icon: display-code
---

# Tool Notes

## [RestrictedPython](https://restrictedpython.readthedocs.io/en/latest/)

RestrictedPython is a tool that allows you to execute Python code in a restricted environment. It is useful for running untrusted code, such as code submitted by users in a web application.

RestrictedPython generally disallows calls to any library that is not explicit whitelisted. 


## [gVisor](https://gvisor.dev/)

What does it do?

gVisor provides a virtualized environment in order to sandbox containers. The system interfaces normally implemented by the host kernel are moved into a distinct, per-sandbox application kernel in order to minimize the risk of a container escape exploit.

### Approach

Previous approaches to isolation:

- Machine-level virtualization: This is the most secure form of isolation, but it is also the most resource-intensive. Each VM has its own kernel and is isolated from the host machine. This is the most secure form of isolation but it is also the most resource-intensive and slowest

- Rule-based isolation: This is a less resource-intensive approach. It uses rules to filter system calls. This is less secure than machine-level virtualization because it is difficult to define rules for arbitrary applications.

gVisor intercepts application system calls and acts as the guest kernel, without the need for translation through virtualized hardware. However, this comes at the price of reduced application compatibility and higher per-system call overhead.

**Different components of gVisor**

- Sentry: This is the part of gVisor that intercepts system calls and emulates the Linux kernel. It is responsible for handling system calls and managing the application's memory.

- Gofer: This is the part of gVisor that manages file system access. It is responsible for translating file system operations into host kernel operations.


**runsc vs runc**

- runc is the default container runtime for Docker and Kubernetes. It is a lightweight, portable container runtime that is designed to be compatible with the Open Container Initiative (OCI) specification.

- runsc is an executable that allows you to run sandboxed containers. It acts as the interface between container runtimes like Docker or Kubernetes and a sandbox environment. 









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

Takeaways:
- Using plugins saves you development time, since it’s faster to install and configure a plugin than it is to recreate the same functionality from scratch.
- The general process for using a plugin is to install it, configure it in your gatsby-config.js file, and then use it in your site as needed.


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