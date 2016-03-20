# &lt;p:nvGrpSpPr&gt;

Non-Visual Properties for a Group Shape

#### Description

This element specifies all non-visual properties for a group shape. This element is a container for the non-visual identification properties, shape properties and application properties that are to be associated with a group shape. This allows for additional information that does not affect the appearance of the group shape to be stored.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_GroupShapeNonVisual

#### Parent Elements

`<p:grpSp>` & `<p:spTree>`

#### Child Elements

Name         | Occ    | Type                                  | Description
------------ | ------ | ------------------------------------- | ----------------------------
p:cNvPr      | [1..1] | a:CT_NonVisualDrawingProps            | Non-Visual Drawing Properties
a:cNvGrpSpPr | [1..1] | a:CT_NonVisualGroupDrawingShapeProps  | Non-Visual Group Shape Drawing Properties
p:nvPr       | [1..1] | p:CT_ApplicationNonVisualDrawingProps | Application Non-Visual Drawing Properties

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_GroupShapeNonVisual">
  <xsd:sequence>
    <xsd:element name="cNvPr" type="a:CT_NonVisualDrawingProps" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="cNvGrpSpPr" type="a:CT_NonVisualGroupDrawingShapeProps" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="nvPr" type="CT_ApplicationNonVisualDrawingProps" minOccurs="1" maxOccurs="1"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_nvGrpSpPr-1.html
https://msdn.microsoft.com/en-us/library/documentformat.openxml.presentation.nonvisualgroupshapeproperties(v=office.15).aspx
