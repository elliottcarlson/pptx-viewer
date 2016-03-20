# &lt;a:xfrm&gt;

2D Transform for Grouped Objects

#### Description

This element represents 2-D transforms for ordinary shapes.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_GroupTransform2D

#### Parent Elements

Name                | Type
------------------- | ----------------------------------
cdr:grpSpPr         | a:CT_GroupShapeProperties
a:grpSpPr           | a:CT_GroupShapeProperties
draw-ssdraw:grpSpPr | a:CT_GroupShapeProperties
p:grpSpPr           | a:CT_GroupShapeProperties

#### Child Elements

Name    | Occ    | Type                | Description
------- | ------ | ------------------- | ----------------------------
a:off   | [0..1] | a:CT_Point2D        | Offset
a:ext   | [0..1] | a:CT_PositiveSize2D | Extents
a:chOff | [0..1] | a:CT_Point2D        | Child Offset
a:chExt | [0..1] | a:CT_PositiveSize2D | Child Extents

#### Attributes

Name   | Occ    | Type        | Description     | Default
------ | ------ | ----------- | --------------- | -------
rot    | [0..1] | a:ST_Angle  | Rotation        | "0"
flipH  | [0..1] | xsd:boolean | Horizontal Flip | "false"
flipV  | [0..1] | xsd:boolean | Vertical Flip   | "false"

#### Schema

```
<xsd:complexType name="CT_GroupTransform2D">
  <xsd:sequence>
    <xsd:element name="off" type="CT_Point2D" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="ext" type="CT_PositiveSize2D" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="chOff" type="CT_Point2D" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="chExt" type="CT_PositiveSize2D" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="rot" type="ST_Angle" use="optional" default="0"/>
  <xsd:attribute name="flipH" type="xsd:boolean" use="optional" default="false"/>
  <xsd:attribute name="flipV" type="xsd:boolean" use="optional" default="false"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_xfrm-5.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.transformgroup.aspx
https://msdn.microsoft.com/en-us/library/documentformat.openxml.drawing.transform2d(v=office.15).aspx
