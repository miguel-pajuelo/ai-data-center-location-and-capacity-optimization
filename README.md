# AI Compute Capacity Optimization

Mixed-integer optimization of an inference computing infrastructure across Europe and the United States. This academic project models where to activate data centers, which GPU nodes to install, and how to allocate demand while respecting latency, capacity, budget, and resilience constraints.

## Model

- **Objective**: minimize data-center activation, hardware and electricity costs over 2027�2029.
- **Decisions**: active locations, integer numbers of H100, H200 and B200 nodes, and workload allocation by market, location and technology.
- **Constraints**: demand coverage, 60 ms latency, 80% maximum utilization, power and hardware availability, a �18 million CAPEX budget and geographic resilience.
- **Tools**: Python, Pyomo, Gurobi and pandas.

The case uses fixed input data from the course project. Electricity costs cover 1,095 days without discounting, following the supplied formulation. Energy coefficients already include PUE.

## Result

The solver finds an optimal cost of **�16.206904 million**, including �15.24 million in CAPEX. The solution activates Madrid, Eemshaven, Columbus and Dallas with 29 nodes. The notebook contains the workload allocation, cost breakdown and constraint checks.

## Run

Install Python, Jupyter, Pyomo, pandas and gurobipy. A valid Gurobi license is required.

```bash
pip install jupyter pyomo pandas gurobipy
jupyter notebook Proyecto_Final_Optimizacion.ipynb
```

Run the cells in order. All case data are embedded in the notebook. This is a classroom case study, with no claim of affiliation with OpenAI.
