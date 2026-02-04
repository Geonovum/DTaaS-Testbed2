# Results

<figure id="r1">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/Testbed_2_Geen_achtergrond_geen_logo.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/Testbed_2_Geen_achtergrond_geen_logo.png" alt=""></a>
<figcaption>resulting ecosystem</figcaption>
</figure>

In general all parties expressed the fact that the testbed cultivated a culture of respect and cooperation between all involved parties. 
Multiple parties discovered new opportunities and connections through this testbed. Because of the different topics addressed in the testbed, parties also got to meet other organisations that typically work in other areas of the Digital Twin ecosystem. Bringing those parties together via the testbed resulted in better understanding of the end-to-end flow and breath of topics in the ecosystem.

There were also some concerns about the length of the testbed. Early on this resulted in a 'lack of urgency' and some tough decisions and much needed clarity was only reached relatively late in the process, which added to missed opportunities in the later stages.


### Archimate

The solutions are documented in <a href="https://geonovum.github.io/DTaaS-Testbed2/archimate/index.html?view=id-be896198ad4447aeb128a1a7ea7c82f1" target="_blank">Archimate</a>.



## Foundation

### Catalogues with Interoperable API's (5.1)

For interoperable API's the testbed required implementations of OGC API Records in combination with the DCAT-AP-NL profile.
While this sounded like a clear brief to the implementing parties, the reality is that both standards allow quite some space for interpretation.
When using Catalogues primarily as a user via the User Interface this wiggle room is easily overcome. However if you want to consume this catalogue 'machine-to-machine', like in a viewer (topic 6.1 'Find and Bind') it turns out this variability is problematic.

It took a while for the involved parties to address this properly, which meant that a complete detailed profile how to implement DCAT-AP-NL in OGC API Records is not realized in scope of this testbed. Never the less, this insight is a valuable lesson from this testbed. 

Another insight is the fact that a DCAT-AP-NL (as well as an ISO-19115) metadata file can contain a lot of detailed information. From a user interface perspective it is quite challenging to address this full breath of detail in a panel in a viewer. Profile negotiation with a limited initial profile and additional profiles for full details might help in this respect.

- Triply

    Triply implemented the OGC API Records interface on top of their Linked Data triple store solution using JSON-LD contexts and JSON-LD frames. 

- Purple Polar Bear

    Purple Polar Bear implemented the OGC API Records interface on top of their solution that focusses on data integration and data interoperability. 

- Future Insight

    Future Insight adapted their existing catalog framework, that already used a different DCAT profile to serve DCAT-AP-NL conform to the OGC API Records interface.

 The <a href="https://geonovum.github.io/DTaaS-Testbed2/archimate/index.html?view=id-e190ac8e3d5e4bc8905d1d92b4ff62da" target="_blank" >archimate view for 'find and bind'</a> documents the interoperable connections that are realized between catalogs and viewers in scope of this testbed.   

### Sharing Data under Conditions, from a data consumer perspective (5.2)

- Future Insight

   For this topic, a <a href="https://github.com/Geonovum/DTaaS-Testbed2/blob/main/deliverables/Report_Data_Sharing_Under_Conditions.pdf" target="_blank">__report__</a> has been written. It examines three foundational enablers of sovereign and policy-driven data exchange: Data Spaces, the iSHARE trust and authorization framework, and Federated Catalogue Services (FSC). This report synthesizes the functional, technical, governance, and legal requirements necessary to support such controlled data exchange. 


## Visualization

### Find and Bind (6.1)

All solutions provide integration with one or more catalogues. 
The <a href="https://geonovum.github.io/DTaaS-Testbed2/archimate/index.html?view=id-e190ac8e3d5e4bc8905d1d92b4ff62da" target="_blank" >archimate view for 'find and bind'</a> documents the interoperable connections that are realized between catalogs and viewers in scope of this testbed.   

- Analyze

<figure id="r2">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/analyze-findbind.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/analyze-findbind.png" alt=""></a>
<figcaption>Analyze Find and Bind screenshot</figcaption>
</figure>


- Imagem

<figure id="r3">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/imagem-findbind.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/imagem-findbind.png" alt=""></a>
<figcaption>Imagem Find and Bind screenshot</figcaption>
</figure>

- iLabs

<figure id="r4">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/iLabs-findbind-2.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/iLabs-findbind-2.png" alt=""></a>
<figcaption>iLabs Find and Bind screenshot</figcaption>
</figure>

### Export & import scenes (6.2)

- esri

The requested deliverable was a draft schema/specification of a Export-import specification. Apart from that draft a demo has been built that provides realtime synchronisation between two viewers. 

<figure id="r5">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/3D_Scenes_import_export.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/3D_Scenes_import_export.png" alt=""></a>
<figcaption>Screenshot of Cesium and esri viewers viewport synchronisation</figcaption>
</figure>

The report on this topic can be found <a href="https://github.com/Geonovum/DTaaS-Testbed2/blob/main/deliverables/Digital_Twin_as_a_Service–Testbed_II-Import_Export_Scenes.pdf" target="_blank">__here__</a>.


## Data

### BIM (Design information) for Digital Twins (7.1)

- Future Insight
 
A conversion from IFC to 3D Tiles is demonstrated. In this workflow a selection of relevant IFC classes is made, these are then converted to 3D Tiles and a 3D Tile service is created on the fly. Metadata of this 3D Tileservice is then also published to a catalog, so viewers can find the converted IFC model and add it to a view.

<figure id="r6">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/IFC-to-3DTiles-1.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/IFC-to-3DTiles-1.png" alt=""></a>
<figcaption>IFC selection and publishing</figcaption>
</figure>

<figure id="r7">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/IFC-to-3DTiles-2.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/IFC-to-3DTiles-2.png" alt=""></a>
<figcaption>3D tiles service in a viewer</figcaption>
</figure>

In addition to the demo, a <a href="https://github.com/Geonovum/DTaaS-Testbed2/blob/main/deliverables/Report_BIM.pdf" target="_blank">__report__</a> has also been written that describes the approach and methodology followed.

## Calculation models

### Making calculation modules interoperable using OGC API Processes (8.1)

The brief of this topic was to expose already available calculation models from different parties using the OGC API Processes specification. This way the processes can be used in different viewers rather than only be tied to the viewer provided specifically for this calculation model.

The <a href="https://geonovum.github.io/DTaaS-Testbed2/archimate/index.html?view=id-00e94b953f2b4bf1adb922e3b4f37054" target="_blank">archimate view for 'Making calculation modules interoperable'</a> documents the calculation modules that are realized in scope of this testbed, as well as the viewers that integrated those modules.

- Analyze

    Analyze created a OGC API Processes interface for a 3-30-300 calculation module.

- Clappform

    Clappform created a OGC API Processes interface for their 'Social safefy Index' (Leefbaarometer) calculations.

- Dat.mobility

    Dat.mobility create a OGC API Processes interface for their mobility calculation modules.

General findings from the implementing parties was that input specifications where quite addequate. Ouput specifications are somewhat limited. Apart from specifying the actual output, parties see a lot of value in also being able to specify a legend, a style or a more specific way to consume the output.
Also mechanisms to provide information about how parameters can be defined in a user interface (like sliders, or dropdown lists) would be seen as welcome additions.

### Model orchestration, status quo

- Avineon/Tensing

For this topic, a <a href="https://github.com/Geonovum/DTaaS-Testbed2/blob/main/deliverables/DTaas2_Orchestration-Avineon_Tensing.pdf" target="_blank">__report__</a> has been written. As shown in the picture below, a maturity model is introduced in this report that defines different levels of orchestration.

<figure id="r8">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/orchestration-maturity-model.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/orchestration-maturity-model.png" alt=""></a>
<figcaption>Orchestration maturity model</figcaption>
</figure>


## Logging and Provenance

Apart from the topics for this particular testbed, a research project on Logging and Provenance has also been held. This was tightly linked to the Digital Twin ecosystem, so we are including it here for reference as well.

<figure id="r9">
<a href="https://geonovum.github.io/DTaaS-Testbed2/media/extensie-metadata.drawio.png" target="_blank"><img src="https://geonovum.github.io/DTaaS-Testbed2/media/extensie-metadata.drawio.png" alt=""></a>
<figcaption>extensions for logging and provenance</figcaption>
</figure>

Desk research was done by Geonovum with stakeholder from Logius and BZK. A practical implementationtest was done with:
- Imagem
- Tygron
- Nelen & Schuurmans

[Onderzoek logboek dataverwerkingen voor (geo) objecten](https://geonovum.github.io/logboek-dataverwerkingen-voor-objecten/)