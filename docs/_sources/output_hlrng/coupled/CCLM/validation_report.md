# Validation report for '`CCLM_Eurocordex`'

## General information

|||
|---|---|
|||
|Created at:                    |`2023-03-01 11:48:16`|
|Created for output directory:  |`/scratch/usr/mvkkarst/test_area`|
|                               |`/hlrng_example/output/coupled`|
|                               |`/CCLM_Eurocordex`|
|Start date:                    |`19590101`|
|End date:                      |`19590110`|
|User:                          |`mvkkarst`|



    
### Report description


This is an example for the post-processing configuration.


    

### Model description

<hr style="border:1px solid gray">

<h4 style="background-color: rgba(31, 119, 180, 0.5);"><b>`model1`</b></h4>



### Performed tasks

<hr style="border:1px solid gray">


#### **Two-dimensional seasonal means**

This task generates figures containing two-dimensional seasonal means $\langle \phi \rangle_S(x,y)$ for a season $s$ and a three-dimensional variable $\phi(x,y,t)$, i.e.$$ \langle \phi \rangle_S(x,y) = \frac{1}{N_S} \sum_{t\in S} \phi(x,y,t), $$where $t$ are all time steps that are contained in season $S$. The number of these time steps is given by $N_S$, where the considered time period is from `19590101` to `19590110`.


#### **Two-dimensional seasonal anomalies**

This task generates figures containing two-dimensional seasonal anomalies $\langle \Delta \phi \rangle_S(x,y)$ for a season $s$, a three-dimensional variable $\phi(x,y,t)$ and a three-dimensional reference field $\phi_{\mathrm{ref}}(x,y,t)$ i.e.$$ \langle \Delta \phi \rangle_S(x,y) = \frac{1}{N_S} \sum_{t\in S} \phi(x,y,t) - \phi_{\mathrm{ref}}(x,y,t) = \langle \phi \rangle_S(x,y) - \langle \phi_{\mathrm{ref}} \rangle_S(x,y) , $$where $t$ are all time steps that are contained in season $S$. The number of these time steps is given by $N_S$, where the considered time period is from `19590101` to `19590110`.


#### **Stations and Regions**

This task generates an image with the configured staitons and regions for which time series data is generated.For regions the time series is generated as the spatial mean over this region.Whereas for stations a remapping to the nearest neighboring grid cell is performed.


#### **Time series**

This task generates figures of temporal means according to the configured time-series operators, e.g. if you specfied `time_series_operators = ["-monmean"]`, a plot with monthly means is generated.Please refer to the `cdo` documentation for more information on these operators.If there are more than 100 samples in the time series and it is compared to reference data, a scatter plot is generated, where the $x$ and $y$ coordinates correspond to the reference samples and the model ones, respectively.


#### **Taylor Diagrams**

Taylor diagrams graphically indicate which of several model data represents best a given reference data.In order to quantify the degree of correspondence between the modeled and observed behavior in terms of three statistics:the Pearson correlation coefficient, the root-mean-square error (RMSE) error, and the standard deviation.Here both data, model and reference, consist of the same number of samples that correspond to a time series starting from `19590101` and ending at `19590110`.


#### **Cost functions**

The cost function $c$ as it is defined here, further summarizes the information given in a Taylor diagram.It measures the root means square error $\epsilon = \sqrt{\frac{1}{N}\sum_{t=t_1}^{t_{N}} (\phi(t)-\phi_{\mathrm{ref}}(t))^2}$ of the model data $\phi(t)$in units of the standard deviation $\sigma_{\mathrm{ref}}$ of reference data $\phi_{\mathrm{ref}}(t)$, i.e.$$ c = \epsilon / \sigma_{\mathrm{ref}}. $$Both data consist of $N$ samples corresponding to a time series starting from $t_1$ and ending at $t_N$.


#### **Vertical profiles**

This task generates vertical profiles of a four-dimensional field $\phi(x, y, z, t)$ at configured stations (using remapping to nearest neighbors) accompanied by performing the configured seasonal means.Vertical profiles that correspong to regions are created by an additional spatial mean over the particular region.




## Results



### 2 meter air temperature (T_2M_AV)   

<hr style="border:2px solid gray">

<details>
<summary><b><i>Analysis</i></b></summary>

    

#### **Description**

This parameter is the temperature of the air near the surface. The corresponding model output variable is called T_2M_AV.

#### **Reference description**





<details>
<summary><i> Postprocess settings for variable 2 meter air temperature (T_2M_AV) </i></summary>

[**Go to settings ->**](../../../global_settings.py)

    
##### seasons
`{'year': ''}`

<hr style="border:1px solid gray">

##### percentiles
`[]`

<hr style="border:1px solid gray">

##### stations
`{'ROSTOCK-WARNEMUNDE': {'lat': '54.18', 'lon': '12.08'}, 'STOCKHOLM': {'lat': '59.35', 'lon': '18.05'}, 'TALLINN': {'lat': '59:23:53', 'lon': '24:36:10'}, 'VISBY': {'lat': '57:40:00', 'lon': '18:19:59'}, 'SUNDSVALL': {'lat': '62:24:36', 'lon': '17:16:12'}, 'LULEA': {'lat': '65:37:12', 'lon': '22:07:48'}, 'VAASA-PALOSAARI': {'lat': '63:06:00', 'lon': '21:36:00'}}`

<hr style="border:1px solid gray">

##### regions
`{'VALID_DOMAIN': {'lat-min': '35.0', 'lat-max': '70.0', 'lon-min': '-10.0', 'lon-max': '35.0'}, 'NORTHERN_LANDS': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Eurocordex/NORTHERN_LANDS.nc'}, 'BALTIC_CATCHMENT': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Eurocordex/BALTIC_CATCHMENT.nc'}, 'NORTHERN_WATERS': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Eurocordex/NORTHERN_WATERS.nc'}, 'BALTIC_SEA': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Baltic/BALTIC_SEA.nc'}, 'BOTHNIAN_GULF': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Baltic/BOTHNIAN_GULF.nc'}, 'BALTIC_PROPER': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Baltic/BALTIC_PROPER.nc'}, 'BELTS': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Baltic/BELTS.nc'}, 'RIGA_FINLAND': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Baltic/RIGA_FINLAND.nc'}, 'NORTH_SEA': {'maskfile': '/scratch/usr/mvkkarst/test_area/hlrng_example/postprocess/CCLM/create_validation_report/../../../reference/masks/Eurocordex/NORTH_SEA.nc'}}`

<hr style="border:1px solid gray">

##### time-series-operators
`['']`

<hr style="border:1px solid gray">

##### plot-config
`{'min_value': 0.0, 'max_value': 15.0, 'delta_value': 1.0, 'contour': True, 'color_map': 'rainbow'}`

<hr style="border:1px solid gray">

##### reference-file-pattern
`../../../reference/coupled/CCLM_Eurocordex/*/T_2M_AV.nc`

<hr style="border:1px solid gray">

##### reference-variable-name
`T_2M_AV`

<hr style="border:1px solid gray">

##### reference-additional-operators
``

<hr style="border:1px solid gray">

##### reference-description
``

<hr style="border:1px solid gray">

##### plot-config-anomaly
`{'min_value': -5.0, 'max_value': 5.0, 'delta_value': 1.0, 'contour': True, 'color_map': 'seismic'}`

<hr style="border:1px solid gray">

##### other-models
`{}`

<hr style="border:1px solid gray">

##### long-name
`2 meter air temperature`

<hr style="border:1px solid gray">

##### description
`This parameter is the temperature of the air near the surface. The corresponding model output variable is called T_2M_AV.`

<hr style="border:1px solid gray">




</details>

    
#### **Two-dimensional seasonal means**

<hr style="border:1px solid gray">

<details>
<summary><b><i>Figures</b></i></summary>

[**Go to notebook ->**](../../../compare_2D_means/results/coupled_CCLM_Eurocordex-19590101_19590110/compare_2D_means.ipynb)



 $\vphantom{M}$

![](./figures/compare_2D_means/T_2M_AV.png)
<figure>
    <figcaption align = "center"> <b> Fig. 1: </b> <b> Seasonal means for variable 2 meter air temperature (T_2M_AV). </b>The rows correspond to different models whereas the columns reflect the various seaons that are considered.The $x$ and $y$ axis measure the longitudes and latitudes, respectively. </figcaption>
</figure>  



</details>


#### **Two-dimensional seasonal anomalies**

<hr style="border:1px solid gray">

<details>
<summary><b><i>Figures</b></i></summary>

[**Go to notebook ->**](../../../compare_2D_anomalies/results/coupled_CCLM_Eurocordex-19590101_19590110/compare_2D_anomalies.ipynb)



 $\vphantom{M}$

![](./figures/compare_2D_anomalies/T_2M_AV.png)
<figure>
    <figcaption align = "center"> <b> Fig. 2: </b> <b> Seasonal anomalies for variable 2 meter air temperature (T_2M_AV). </b>The rows correspond to different models whereas the columns reflect the various seaons that are considered.The $x$ and $y$ axis measure the longitudes and latitudes, respectively. </figcaption>
</figure>  



</details>


#### **Stations and Regions**

<hr style="border:1px solid gray">

<details>
<summary><b><i>Figures</b></i></summary>

[**Go to notebook ->**](../../../draw_stations_and_regions/results/coupled_CCLM_Eurocordex-19590101_19590110/draw_stations_and_regions.ipynb)



 $\vphantom{M}$

![](./figures/draw_stations_and_regions/T_2M_AV.png)
<figure>
    <figcaption align = "center"> <b> Fig. 3: </b> <b> Stations and regions for variable 2 meter air temperature (T_2M_AV). </b>Colored areas depict the different regions. The dots are located at the station's coordinates. </figcaption>
</figure>  



</details>


#### **Time series**

<hr style="border:1px solid gray">

<details>
<summary><b><i>Figures</b></i></summary>

[**Go to notebook ->**](../../../compare_time_series/results/coupled_CCLM_Eurocordex-19590101_19590110/compare_time_series.ipynb)



 $\vphantom{M}$

![](./figures/compare_time_series/T_2M_AV-stations.png)
<figure>
    <figcaption align = "center"> <b> Fig. 4: </b> <b>Time series for variable 2 meter air temperature (T_2M_AV). </b>Shaded areas depict the $\pm 2 \sigma$ vicinity (approximately the 95% confidence interval) around the mean values. </figcaption>
</figure>  



 $\vphantom{M}$

![](./figures/compare_time_series/T_2M_AV-regions.png)
<figure>
    <figcaption align = "center"> <b> Fig. 5: </b> <b>Time series for variable 2 meter air temperature (T_2M_AV). </b>Shaded areas depict the $\pm 2 \sigma$ vicinity (approximately the 95% confidence interval) around the mean values. </figcaption>
</figure>  



</details>


#### **Taylor Diagrams**

<hr style="border:1px solid gray">

<details>
<summary><b><i>Figures</b></i></summary>

[**Go to notebook ->**](../../../create_taylor_diagrams/results/coupled_CCLM_Eurocordex-19590101_19590110/create_taylor_diagrams.ipynb)



 $\vphantom{M}$

![](./figures/create_taylor_diagrams/T_2M_AV-stations.png)
<figure>
    <figcaption align = "center"> <b> Fig. 6: </b> <b> Taylor diagrams for variable 2 meter air temperature (T_2M_AV). </b>Colored stars stand for the model result and the black circle is the reference.The standard deviation of the data is measured on the radial axis whereas the correaltion to the reference is given by the angle;depicted is the arcus cosine of the angle.The colormap refers to the root means square error of the model data with respect to the reference data.The rows correspond to the different regions and stations whereas the columns are related to the different kind of time series. </figcaption>
</figure>  



 $\vphantom{M}$

![](./figures/create_taylor_diagrams/T_2M_AV-regions.png)
<figure>
    <figcaption align = "center"> <b> Fig. 7: </b> <b> Taylor diagrams for variable 2 meter air temperature (T_2M_AV). </b>Colored stars stand for the model result and the black circle is the reference.The standard deviation of the data is measured on the radial axis whereas the correaltion to the reference is given by the angle;depicted is the arcus cosine of the angle.The colormap refers to the root means square error of the model data with respect to the reference data.The rows correspond to the different regions and stations whereas the columns are related to the different kind of time series. </figcaption>
</figure>  



</details>


#### **Cost functions**

<hr style="border:1px solid gray">

<details>
<summary><b><i>Figures</b></i></summary>

[**Go to notebook ->**](../../../get_cost_function/results/coupled_CCLM_Eurocordex-19590101_19590110/get_cost_function.ipynb)



 $\vphantom{M}$

![](./figures/get_cost_function/T_2M_AV-stations.png)
<figure>
    <figcaption align = "center"> <b> Fig. 8: </b> <b> Cost functions $c$ for variable 2 meter air temperature (T_2M_AV). </b>The colors refer to the magnitude of the cost function: green means very good $( 0 \leq c < 1 )$,yellow stands for satisfactory $( 1 < c < 2 )$ and red shows bad quality $( c \geq 2 )$.<b>Bold</b> numbers correspond to the best performing model, whereas <i>italic</i> number refer to the worst performing model for that particular station/region and kind of time series.The rows correspond to the different regions and stations whereas the columns are related to the different temporal means and models. </figcaption>
</figure>  



 $\vphantom{M}$

![](./figures/get_cost_function/T_2M_AV-regions.png)
<figure>
    <figcaption align = "center"> <b> Fig. 9: </b> <b> Cost functions $c$ for variable 2 meter air temperature (T_2M_AV). </b>The colors refer to the magnitude of the cost function: green means very good $( 0 \leq c < 1 )$,yellow stands for satisfactory $( 1 < c < 2 )$ and red shows bad quality $( c \geq 2 )$.<b>Bold</b> numbers correspond to the best performing model, whereas <i>italic</i> number refer to the worst performing model for that particular station/region and kind of time series.The rows correspond to the different regions and stations whereas the columns are related to the different temporal means and models. </figcaption>
</figure>  



</details>



</details>

