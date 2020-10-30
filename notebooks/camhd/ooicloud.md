### OOICloud Overview

#### Columbia University and Queens College CUNY

The [OOICloud Project](https://github.com/ooicloud) is making data from the Ocean Observatories Initiative ([OOI](https://oceanobservatories.org)) publically available on Microsoft Azure Open Datasets and accessible through a [Pangeo](http://pangeo.io/) interface. A primary goal of the project is to provide these data to the scientific community using a cloud-performant object storage model, and to provide large-scale data-proximate compute capabilities for research investigations. The OOI sensor network comprises 89 scientific platforms with approximately 830 instruments, and provides nearly 5 TB of data each month for the study of the ocean-atmosphere system from the continental margins to the mid-ocean ridges. A core component of OOI is the [Regional Cabled Array](https://oceanobservatories.org/regional-cabled-array/) which uses a fiber-optic cable to connect and power the largest array of netwoked oceanographic instruments in the world, delivering data in real-time to shore. 

[CamHD](https://oceanobservatories.org/instrument-class/camhd/) is a high-definition video camera connected to the OOI's fiber optic cable at Axial Seamount and provides data that can support a wide range of oceanographic, biological and geophysical investigations. Every three hours the camera scans a hydrothermal vent chimney, imaging the entire chimney over the course of about fifteen minutes. This [Jupyter notebook](https://github.com/ooicloud/ooi-pangeo/blob/master/notebooks/camhd/ooi_camhd_azure.ipynb) shows how to load video data from CamHD and demonstrates the basic usage of the pycamhd library, which can be used to extract frames from the ProRes encoded Quicktime files. 


#### Storage resources 

All available video files are listed in a [JSON file](https://ooiopendata.blob.core.windows.net/camhd/dbcamhd.json) that has useful information such as the Unix timestamp (seconds) of the first frame in each video, and the total number of frames in each video. Data are stored as bock blobs on Azure Blob storage in the following  container:

`https://ooiopendata.blob.core.windows.net/camhd`

Large-scale processing using this dataset is best performed in the East US Azure data center, where the data are stored. Computational resources are available at [ooi.pangeo.io](https://ooi.pangeo.io/)


#### Pretty picture

<img src="https://oceanobservatories.org/wp-content/uploads/2016/01/HD_Camera_Thermisor_OSMO.jpg" width=650px;><br/>

<p style="font-size:80%;margin-left:15px;">The HD camera (orange triangular frame) images the 14 ft-tall actively venting hot spring deposit ‘Mushroom’ located within the caldera for Axial Seamount. The vent rests on an old lava flow. Radiating cracks in the flow are filled with white bacterial mats and small tube worms, marking sites of diffusely flowing fluids that issue from the fractures in the basalt. The 3-D temperature array in the background encloses a tube worm bush, sending 24 temperature measurements live to shore every second.</p>


#### Contact

For questions about this dataset, contact [`aiforearthdatasets@microsoft.com`](mailto:aiforearthdatasets@microsoft.com?subject=ghe%20question).


#### Notices

MICROSOFT PROVIDES AZURE OPEN DATASETS ON AN "AS IS" BASIS. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, GUARANTEES OR CONDITIONS WITH RESPECT TO YOUR USE OF THE DATASETS. TO THE EXTENT PERMITTED UNDER YOUR LOCAL LAW, MICROSOFT DISCLAIMS ALL LIABILITY FOR ANY DAMAGES OR LOSSES, INCLUDING DIRECT, CONSEQUENTIAL, SPECIAL, INDIRECT, INCIDENTAL OR PUNITIVE, RESULTING FROM YOUR USE OF THE DATASETS. 

This dataset is provided under the original terms that Microsoft received source data. The dataset may include data sourced from Microsoft.
