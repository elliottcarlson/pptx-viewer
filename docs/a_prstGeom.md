# &lt;a:prstGeom&gt;

Shape Properties

#### Description

This element specifies when a preset geometric shape should be used instead of a custom geometric shape. The generating application should be able to render all preset geometries enumerated in the ST_ShapeType list.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_PresetGeometry2D

#### Parent Elements

Name             | Type
---------------- | ----------------------------------
n/a              | a:EG_Geometry
draw-chart:spPr  | a:CT_ShapeProperties
cdr:spPr         | a:CT_ShapeProperties
draw-diag:spPr   | a:CT_ShapeProperties
a:spPr           | a:CT_ShapeProperties
draw-pic:spPr    | a:CT_ShapeProperties
draw-ssdraw:spPr | a:CT_ShapeProperties
p:spPr           | a:CT_ShapeProperties

#### Child Elements

Name        | Occ    | Type               | Description
----------- | ------ | ------------------ | ---------------------------
a:avLst     | [0..1] | a:CT_GeomGuideList | List of Shape Adjust Values

#### Attributes

Name   | Occ    | Type           | Description  | Default
------ | ------ | -------------- | ------------ | -------
prst   | [1..1] | a:ST_ShapeType | Preset Shape | 

#### Schema

```
<xsd:complexType name="CT_PresetGeometry2D">
  <xsd:sequence>
    <xsd:element name="avLst" type="CT_GeomGuideList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="prst" type="ST_ShapeType" use="required"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_prstGeom-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.presetgeometry.aspx
