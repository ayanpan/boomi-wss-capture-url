# Capture Resource Path from Web Services Server in Boomi

## Problem Statement:
We receive a request in Boomi from an external application via Web Services Server Connector. In this request we have a requirement to extract the resouce path. For example, the incoming URL is https://www.example.com/v1/api/rpath1?query=parameter, and we have to fetch the value **v1/api/rpath1?query=parameter**.

## Solution:
Use the standard Boomi Dynamic Process Property (DPP) of "inpath".

Below are the steps to achieve it.

1. Use a Set Properties Shape.

2. On the Left Hand Side, set DPP = DPP_Get_ResourcePath

3. On the Right Hand Side, get from DPP and put DPP Name as **inpath**.
