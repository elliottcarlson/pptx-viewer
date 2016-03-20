# &lt;p:nvSpPr&gt;

Non-Visual Properties for a Shape

#### Description

This element specifies all non-visual properties for a shape. This element is a container for the non-visual identification properties, shape properties and application properties that are to be associated with a shape. This allows for additional information that does not affect the appearance of the shape to be stored.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_ShapeNonVisual

#### Parent Elements

Name  | Type
----- | ----------
p:sp  | p:CT_Shape

#### Child Elements

Name      | Occ    | Type                                  | Description
--------- | ------ | ------------------------------------- | -----------------------------------------
p:cNvPr   | [1..1] | a:CT_NonVisualDrawingProps            | Non-Visual Drawing Properties
p:cNvSpPr | [1..1] | a:CT_NonVisualDrawingShapeProps       | Non-Visual Drawing Properties for a Shape
p:nvPr    | [1..1] | p:CT_ApplicationNonVisualDrawingProps | Application Non-Visual Drawing Properties

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_ShapeNonVisual">
  <xsd:sequence>
    <xsd:element name="cNvPr" type="a:CT_NonVisualDrawingProps" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="cNvSpPr" type="a:CT_NonVisualDrawingShapeProps" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="nvPr" type="CT_ApplicationNonVisualDrawingProps" minOccurs="1" maxOccurs="1"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_nvSpPr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.spreadsheet.nonvisualshapeproperties.aspx
