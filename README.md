# dsx

# Prepare
1. clone this project
```
git clone https://github.com/ibmcloudprivate2/dsx.git
```
2. change folder 
```
cd dsx
```

## walkthrough of demo

1. deploy dsx from the IBM Cloud Private Catalog
- specify a **'Release name'** of your choice
- choose your choice of namespace 
- enter 'true' for useDynamicProvisioning

[watch video](https://youtu.be/eH9IwyUqLRU)

2. From Workloads > Helm Releases 
- search for the release name used above and click on the release **Name** to drill down on details of deployment
- ensure **"Persistent Volume Claim"** Status is **Bound**
- ensure the **Available** for all deployment is 1

**Deployment**

| NAME	| DESIRED	| CURRENT	| UP TO DATE	| AVAILABLE	| AGE | 
| -------------| -------------| -------------| -------------| -------------| ------------- |
| dsx-ux-server	| 1	| 1	| 1	|1 | 50m |
| notebook-server	| 1	| 1	| 1	|1 | 50m |
| rstudio-server	| 1	| 1	| 1	|1 | 50m |
| zeppelin-server	| 1	| 1	| 1	|1 | 50m |

3. To access the DSX Dashboad
- under **Service** Section
- click on **dsx-ux** to drill down the service details
- click on the **Node Port** endpoint listed to acceess the DSX Dashboard

4. From menu > My Notebooks > add notebooks > 
a) From URL or
- enter **Name** of your choice : *sample* 

```
https://raw.githubusercontent.com/ibmcloudprivate2/dsx/master/sample.ipynb
```
b) File > Open > Upload > sample.ipynb

5. Upload sample data
- File > Open > Upload > school_earnings.csv

6. Run it, Cell > Run All
- it will take a while to execute for each cell
- cell with [`*`] means the cell is still being executed
- cell with a number in [ 2 ] means the execution of codes in cell is completed

# Reference
- [Jupyter Notebook Tutorial in Python](https://plot.ly/python/ipython-notebook-tutorial/)


