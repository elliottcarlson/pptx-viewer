# &lt;a:custGeom&gt;

Custom Geometry

#### Description

This element specifies the existence of a custom geometric shape. This shape consists of a series of lines and curves described within a creation path. In addition to this there can also be adjust values, guides, adjust handles, connection sites and an inscribed rectangle specified for this custom geometric shape.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_CustomGeometry2D

#### Parent Elements

Name             | Type
---------------- | ----------------------------------
n/a              | a:EG_Geometry
n/a              | a:EG_TextGeometry
draw-chart:spPr  | a:CT_ShapeProperties
cdr:spPr         | a:CT_ShapeProperties
draw-diag:spPr   | a:CT_ShapeProperties
a:spPr           | a:CT_ShapeProperties
draw-pic:spPr    | a:CT_ShapeProperties
draw-ssdraw:spPr | a:CT_ShapeProperties
p:spPr           | a:CT_ShapeProperties

#### Child Elements

Name       | Occ    | Type                    | Description
---------- | ------ | ----------------------- | ------------------------------
a:avLst    | [0..1] | a:CT_GeomGuideList      | Adjust Value List
a:gdLst    | [0..1] | a:CT_GeomGuideList      | List of Shape Guides
a:ahLst    | [0..1] | a:CT_AdjustHandleList   | List of Shape Adjust Handles
a:cxnLst   | [0..1] | a:CT_ConnectionSiteList | List of Shape COnnection Sites
a:rect     | [0..1] | a:CT_GeomRect           | Shape Text Rectangle
a:pathList | [1..1] | a:CT_Path2DList         | List of Shape Paths

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_CustomGeometry2D">
  <xsd:sequence>
    <xsd:element name="avLst" type="CT_GeomGuideList" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="gdLst" type="CT_GeomGuideList" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="ahLst" type="CT_AdjustHandleList" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="cxnLst" type="CT_ConnectionSiteList" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="rect" type="CT_GeomRect" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="pathLst" type="CT_Path2DList" minOccurs="1" maxOccurs="1"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_custGeom-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.customgeometry.aspx
