# &lt;a:gradFill&gt;

Gradient Fill

#### Description

This element defines a gradient fill.

A gradient fill is a fill which is characterized by a smooth gradual transition from one color to the next. At its simplest, it is a fill which transitions between two colors; or more generally, it can be a transition of any number of colors.

The desired transition colors and locations are defined in the gradient stop list (gsLst) child element.

The other child element defines the properties of the gradient fill (there are two styles-- a linear shade style as well as a path shade style)

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_GradientFillProperties

#### Parent Elements

Name                | Type
------------------- | ---------------------------------
n/a                 | a:EG_FillProperties
n/a                 | a:EG_LineFillProperties
a:bgFillStyleLst    | a:CT_BackgroundFillStyleList
draw-diag:bg        | a:CT_BackgroundFormatting
a:fill              | a:CT_FillEffect
a:fillOverlay       | a:CT_FillOverlayEffect
a:fill              | a:CT_FillProperties
a:fillStyleLst      | a:CT_FillStyleList
a:tcPr              | a:CT_TableCellProperties
a:tblPr             | a:CT_TableProperties
a:uFill             | a:CT_TextUnderlineFillGroupWrapper
p:bgPr              | p:CT_BackgroundProperties
cdr:grpSpPr         | a:CT_GroupShapeProperties
a:grpSpPr           | a:CT_GroupShapeProperties
draw-ssdraw:grpSpPr | a:CT_GroupShapeProperties
p:grpSpPr           | a:CT_GroupShapeProperties
a:endParaRPr        | a:CT_TextCharacterProperties
a:rPr               | a:CT_TextCharacterProperties
a:defRPr            | a:CT_TextCharacterProperties
a:rPr               | a:CT_TextCharacterProperties
draw-chart:spPr     | a:CT_ShapeProperties
cdr:spPr            | a:CT_ShapeProperties
draw-diag:spPr      | a:CT_ShapeProperties
a:spPr              | a:CT_ShapeProperties
draw-pic:spPr       | a:CT_ShapeProperties
draw-ssdraw:spPr    | a:CT_ShapeProperties
p:spPr              | a:CT_ShapeProperties
a:ln                | a:CT_LineProperties
a:lnL               | a:CT_LineProperties
a:lnR               | a:CT_LineProperties
a:lnT               | a:CT_LineProperties
a:lnB               | a:CT_LineProperties
a:lnTlToBr          | a:CT_LineProperties
a:lnBlToTr          | a:CT_LineProperties
a:uLn               | a:CT_LineProperties

#### Child Elements

Name        | Occ    | Type                       | Description
----------- | ------ | -------------------------- | ------------------------------------
a:gsLst     | [0..1] | a:CT_GradientStopList      | RGB Color Model - Percentage Variant
a:lin       | [0..1] | a:CT_LinearShadeProperties | Linear Gradient Fill
a:path      | [0..1] | a:CT_PathShadeProperties   | Path Gradient
a:tileRect  | [0..1] | a:CT_RelativeRect          | Tile Rectangle

#### Attributes

Name         | Occ    | Type              | Description       | Default
------------ | ------ | ----------------- | ----------------- | -------
flip         | [0..1] | a:ST_FileFlipMode | Tile Flip         | 
rotWithShape | [0..1] | xsd:boolean       | Rotate With Shape | 

#### Schema

```
<xsd:complexType name="CT_GradientFillProperties">
  <xsd:sequence>
    <xsd:element name="gsLst" type="CT_GradientStopList" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="EG_ShadeProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="tileRect" type="CT_RelativeRect" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="flip" type="ST_TileFlipMode" use="optional"/>
  <xsd:attribute name="rotWithShape" type="xsd:boolean" use="optional"/>
</xsd:complexType>

<xsd:group name="EG_ShadeProperties">
  <xsd:choice>
    <xsd:element name="lin" type="CT_LinearShadeProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="path" type="CT_PathShadeProperties" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_gradFill-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.gradientfill.aspx
