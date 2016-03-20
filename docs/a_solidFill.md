# &lt;a:solidFill&gt;

Solid Fill

#### Description

This element specifies a solid color fill. The shape is filled entirely with the specified color.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_SolidColorFillProperties

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

Name        | Occ    | Type             | Description
----------- | ------ | ---------------- | --------------------------------------
a:scrgbClr  | [1..1] | a:CT_ScRgbColor  | RGB Color Model - Percentage Variant
a:srgbClr   | [0..1] | a:CT_SRgbColor   | RGB Color Model - Hex Variant
a:hslClr    | [0..1] | a:CT_HslColor    | Hue, Saturation, Luminance Color Model
a:sysClr    | [0..1] | a:CT_SystemColor | System Color
a:schemeClr | [0..1] | a:CT_SchemeColor | Scheme Color
a:prstClr   | [0..1] | a:CT_PresetColor | Preset Color

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_SolidColorFillProperties">
  <xsd:sequence>
    <xsd:group ref="EG_ColorChoice" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
</xsd:complexType>

<xsd:group name="EG_ColorChoice">
  <xsd:choice>
    <xsd:element name="scrgbClr" type="CT_ScRgbColor" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="srgbClr" type="CT_SRgbColor" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="hslClr" type="CT_HslColor" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="sysClr" type="CT_SystemColor" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="schemeClr" type="CT_SchemeColor" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="prstClr" type="CT_PresetColor" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_solidFill-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.solidfill.aspx
