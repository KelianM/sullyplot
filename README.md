# sullyplot

The `sullyplot` R Package provides a framework for automated plotting of graphs and dashboards using OpenAI's latest LLMs.

## Usage

You should first set the `OPENAI_API_KEY` environment variable on whichever environment you are using.
If you want to use the Azure OpenAI API, you will also need to set the `AZURE_RESOURCE_NAME` environment variable.

Then simply use the functions from `sullyplot` with `sullyplot::function_name()` to use AI models.

Can be installed using `devtools::install_github("KelianM/sullyplot@main")`.

## Functions

### Automatically design and plot a full dashboard

0. `auto_dash` - Generates a dashboard from the input file and returns the list of `ggplot` objects.
1. `auto_dash_design` - Generates a dataframe describing the design of a dashboard for the given file.

### Automatically plot individual graphs

2. `auto_plot` - Generates a `ggplot` object from an input file, list of necessary columns, and plot description.

### Render generated plots and dashboards
3. `render_dash_html` - Renders a list of `ggplot` objects as an interactive dashboard in html.
4. `render_plot_html` - Renders a `ggplot` object as an interactive html page.
5. `render_dash_pdf` - Renders a list of `ggplot` objects as a pdf file.

### Openai Chat Requests
6. `sullyplot_openai_continue_chat` - Makes a continue chat request with openai chat completion endpoint and tracks token usage.
7. `sullyplot_azure_continue_chat` - Makes a continue chat request with azure openai chat completion endpoint and tracks token usage.