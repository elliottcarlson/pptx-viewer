# &lt;p:cSld&gt;

Common slide data for slides

#### Description

This element specifies a container for slide information that is relevant to all of the slide types. All slides share a common set of properties that is independent of the slide type; the description of these properties for any particular slide is stored within the slide's cSld container. Slide data specific to the slide type indicated by the parent element is stored elsewhere.

#### Element information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_CommonSlideData

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:sld              | p:CT_Slide

#### Child Elements

Name          | Occ    | Type                  | Description
------------- | ------ | --------------------- | ------------------
p:bg          | [0..1] | p:CT_Background       | Slide Background
a:spTree      | [1..1] | p:CT_GroupShape       | Shape Tree
p:custDataLst | [0..1] | p:CT_CustomerDataList | Customer Data List
p:controls    | [0..1] | p:CT_ControlList      | List of Controls
p:extLst      | [0..1] | p:CT_ExtensionList    | Extension List

#### Attributes

Name          | Occ    | Type        | Description                        | Default
------------  | ------ | ----------- | ---------------------------------- | -------
name          | [0..1] | xsd:string  | Slide Name                         | ""

#### Schema

```
<xsd:complexType name="CT_CommonSlideData">
  <xsd:sequence>
    <xsd:element name="bg"          type="CT_Background"       minOccurs="0"/>
    <xsd:element name="spTree"      type="CT_GroupShape"/>
    <xsd:element name="custDataLst" type="CT_CustomerDataList" minOccurs="0"/>
    <xsd:element name="controls"    type="CT_ControlList"      minOccurs="0"/>
    <xsd:element name="extLst"      type="CT_ExtensionList"    minOccurs="0"/>
  </xsd:sequence>
  <xsd:attribute name="name" type="xsd:string" default=""/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_cSld-1.html
https://msdn.microsoft.com/EN-US/library/office/documentformat.openxml.presentation.commonslidedata.aspx
http://python-pptx.readthedocs.org/en/develop/dev/analysis/schema/ct_slide.html
