Here are two diagrams for your PySpark Employee Data Cleaning project:

1. **Flowchart** – Shows the complete execution flow from reading the CSV to displaying cleaned data.
2. **Operations diagram** – Shows each transformation applied to the DataFrame, including null handling, replacement, filtering, and name validation.

## **1. PySpark data cleaning flowchart**

\#chatgpt-mermaid-\_r_oc\_{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;fill:rgb(13, 13, 13);}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#chatgpt-mermaid-\_r_oc\_ .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-\_r_oc\_ .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-\_r_oc\_ .error-icon{fill:rgb(243, 243, 243);}#chatgpt-mermaid-\_r_oc\_ .error-text{fill:rgb(13, 13, 13);stroke:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ .edge-thickness-normal{stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .edge-thickness-thick{stroke-width:3.5px;}#chatgpt-mermaid-\_r_oc\_ .edge-pattern-solid{stroke-dasharray:0;}#chatgpt-mermaid-\_r_oc\_ .edge-thickness-invisible{stroke-width:0;fill:none;}#chatgpt-mermaid-\_r_oc\_ .edge-pattern-dashed{stroke-dasharray:3;}#chatgpt-mermaid-\_r_oc\_ .edge-pattern-dotted{stroke-dasharray:2;}#chatgpt-mermaid-\_r_oc\_ .marker{fill:rgb(143, 143, 143);stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_oc\_ .marker.cross{stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_oc\_ svg{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;}#chatgpt-mermaid-\_r_oc\_ p{margin:0;}#chatgpt-mermaid-\_r_oc\_ .label{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ .cluster-label text{fill:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ .cluster-label span{color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ .cluster-label span p{background-color:transparent;}#chatgpt-mermaid-\_r_oc\_ .label text,#chatgpt-mermaid-\_r_oc\_ span{fill:rgb(13, 13, 13);color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ .node rect,#chatgpt-mermaid-\_r_oc\_ .node circle,#chatgpt-mermaid-\_r_oc\_ .node ellipse,#chatgpt-mermaid-\_r_oc\_ .node polygon,#chatgpt-mermaid-\_r_oc\_ .node path{fill:rgb(222, 234, 251);stroke:rgb(83, 154, 248);stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .rough-node .label text,#chatgpt-mermaid-\_r_oc\_ .node .label text,#chatgpt-mermaid-\_r_oc\_ .image-shape .label,#chatgpt-mermaid-\_r_oc\_ .icon-shape .label{text-anchor:middle;}#chatgpt-mermaid-\_r_oc\_ .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .rough-node .label,#chatgpt-mermaid-\_r_oc\_ .node .label,#chatgpt-mermaid-\_r_oc\_ .image-shape .label,#chatgpt-mermaid-\_r_oc\_ .icon-shape .label{text-align:center;}#chatgpt-mermaid-\_r_oc\_ .node.clickable{cursor:pointer;}#chatgpt-mermaid-\_r_oc\_ .root .anchor path{fill:rgb(143, 143, 143)!important;stroke-width:0;stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_oc\_ .arrowheadPath{fill:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_oc\_ .edgePath .path{stroke:rgb(143, 143, 143);stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .flowchart-link{stroke:rgb(143, 143, 143);fill:none;}#chatgpt-mermaid-\_r_oc\_ .edgeLabel{background-color:rgb(252, 252, 252);text-align:center;}#chatgpt-mermaid-\_r_oc\_ .edgeLabel p{background-color:rgb(252, 252, 252);}#chatgpt-mermaid-\_r_oc\_ .edgeLabel rect{opacity:0.5;background-color:rgb(252, 252, 252);fill:rgb(252, 252, 252);}#chatgpt-mermaid-\_r_oc\_ .labelBkg{background-color:rgba(252, 252, 252, 0.5);}#chatgpt-mermaid-\_r_oc\_ .cluster rect{fill:rgb(243, 243, 243);stroke:rgba(0, 0, 0, 0.1);stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .cluster text{fill:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ .cluster span{color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:12px;background:rgb(243, 243, 243);border:1px solid rgba(0, 0, 0, 0.1);border-radius:2px;pointer-events:none;z-index:100;}#chatgpt-mermaid-\_r_oc\_ .flowchartTitleText{text-anchor:middle;font-size:18px;fill:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_oc\_ rect.text{fill:none;stroke-width:0;}#chatgpt-mermaid-\_r_oc\_ .icon-shape,#chatgpt-mermaid-\_r_oc\_ .image-shape{background-color:rgb(252, 252, 252);text-align:center;}#chatgpt-mermaid-\_r_oc\_ .icon-shape p,#chatgpt-mermaid-\_r_oc\_ .image-shape p{background-color:rgb(252, 252, 252);padding:2px;}#chatgpt-mermaid-\_r_oc\_ .icon-shape .label rect,#chatgpt-mermaid-\_r_oc\_ .image-shape .label rect{opacity:0.5;background-color:rgb(252, 252, 252);fill:rgb(252, 252, 252);}#chatgpt-mermaid-\_r_oc\_ .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#chatgpt-mermaid-\_r_oc\_ .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#chatgpt-mermaid-\_r_oc\_ .node .neo-node{stroke:rgb(83, 154, 248);}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node rect,#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].cluster rect,#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node polygon{stroke:url(#chatgpt-mermaid-\_r_oc\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].swimlane.cluster rect{filter:none;}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node path{stroke:url(#chatgpt-mermaid-\_r_oc\_-gradient);stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node .outer-path{filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node .neo-line path{stroke:rgb(83, 154, 248);filter:none;}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node circle{stroke:url(#chatgpt-mermaid-\_r_oc\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].node circle .state-start{fill:#000000;}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].icon-shape .icon{fill:url(#chatgpt-mermaid-\_r_oc\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_oc\_ [data-look="neo"].icon-shape .icon-neo path{stroke:url(#chatgpt-mermaid-\_r_oc\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_oc\_ .node text{font-size:14px;font-weight:600;letter-spacing:normal;fill:rgb(0, 79, 153);}#chatgpt-mermaid-\_r_oc\_ .edgeLabels text{font-size:13px;font-weight:600;letter-spacing:-0.08px;fill:rgb(0, 79, 153);}#chatgpt-mermaid-\_r_oc\_ .node tspan[font-weight="normal"],#chatgpt-mermaid-\_r_oc\_ .edgeLabels tspan[font-weight="normal"]{font-weight:600;}#chatgpt-mermaid-\_r_oc\_ .edgeLabel .label rect{opacity:1;rx:13px;ry:13px;fill:rgb(245, 250, 255);stroke:rgb(206, 219, 229);stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .node rect,#chatgpt-mermaid-\_r_oc\_ .node circle,#chatgpt-mermaid-\_r_oc\_ .node ellipse,#chatgpt-mermaid-\_r_oc\_ .node polygon,#chatgpt-mermaid-\_r_oc\_ .node path{fill:rgb(229, 243, 255);stroke:rgba(0, 0, 0, 0.1);stroke-width:1px;}#chatgpt-mermaid-\_r_oc\_ .node rect{rx:16px;ry:16px;}#chatgpt-mermaid-\_r_oc\_ .mermaid-decision .label-container{fill:rgb(245, 250, 255);stroke:rgb(206, 219, 229);stroke-dasharray:2,2;}#chatgpt-mermaid-\_r_oc\_ .edgePaths .flowchart-link{stroke:rgb(143, 143, 143);stroke-width:1px;stroke-linecap:round;stroke-linejoin:round;}#chatgpt-mermaid-\_r_oc\_ .marker{fill:rgb(143, 143, 143);stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_oc\_ :root{--mermaid-font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";}StartImport PySpark LibrariesCreate SparkSessionReadEmployee_Table_1000_Rows.csvCreate PySpark DataFramePrint SchemaDisplay Before CleaningFill Department NULL withGeneralistFill Joining Year NULL with2010Replace Information Tech withITFilter Age less than 60Filter Age greater than 18Validate First Name OR LastName is NOT NULLDisplay After CleaningEnd

## **2. Data cleaning operations diagram**

**Input: Employee CSV**

Employee_Table_1000_Rows.csv

1,000 records

**Operation 1 – Handle NULL values**

Department

`NULL → Generalist`

Joining Year

`NULL → 2010`

**Operation 2 – Standardize department**

`Information Tech → IT`

**Operation 3 – Filter age**

**Age less than 60**

Keep

**Age greater than 18**

Keep

Both conditions must be satisfied. Valid age: 19–59.

**Operation 4 – Validate employee names**

`First Name IS NOT NULL OR Last Name IS NOT NULL`

Keep if at least one name exists

Remove if both names are NULL

**Output: Cleaned DataFrame**

Ready for downstream processing

## **3. PySpark operations reference**

| Operation      | PySpark syntax  | Transformation       |
| -------------- | --------------- | -------------------- |
| Fill NULL      | `na.fill()`     | Missing values       |
| Replace values | `replace()`     | Standardization      |
| Filter         | `filter()`      | Age validation       |
| Validate names | `isNotNull()`   | Data completeness    |
| Display        | `show()`        | Data inspection      |
| Schema         | `printSchema()` | Structure inspection |

## **4. Important correction in your script**

Your current name validation uses:

```
df_pyspark.filter(    df_pyspark['First Name'].isNotNull() |    df_pyspark['Last Name'].isNotNull())
```

The `|` means OR, so a record is retained if at least one name exists.

If you use `&` instead, both names must exist.

**Data Engineering concept:** Your script demonstrates four important data-quality operations: completeness, standardization, validity, and filtering.
