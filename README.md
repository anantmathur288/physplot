# physplot

Plotting and error propagation tools related to lab work for students.

## Usage

Import using: from physplot import Graph, Error, Propagation

1. Graphing:
    - Create figure and plot axes: Graph.plot_details(#row_plots, #col_plots, width, height, ...)
    - Create Graph object: graph_obj = Graph(axs[#row, #col], x, y)
    - Plot and decorate the object: obj.grapher(...) or Graph.grapher(obj, ...)
    - Show graph: Graph.show()
2. Error Data:
    - Create Error object: err_obj = Error(data)
    - Calculate error (can add certain constraints): err = Error.err(err_obj, ...) or err_obj.err(...)
3. Error Propagation:
    - Create Propagation object with 2 methods:
         - Use Error object: prop_obj = Propagation({variable : err_obj}, ...)
         - Use external error data: prop_obj = Propagation(manual_data = data, manual_err = err, ...)
         - Calculate propagated error: Propagation.propagator(prop_obj, expression, ...) or prop_obj.propagator(expression, ...)

## Dependencies
Requires numpy, matplotlib, scipy and sympy (come with installation of physplot)

## Installation
```bash
pip install physplot