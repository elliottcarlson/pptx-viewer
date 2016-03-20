# &lt;a:pattFill&gt;

Pattern Fill

#### Description

This element specifies a pattern fill. A repeated pattern is used to fill the object.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_PatternFillProperties

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

Name     | Occ    | Type       | Description
-------- | ------ | ---------- | ----------------
a:fgClr  | [0..1] | a:CT_Color | Foreground color
a:bgClr  | [0..1] | a:CT_Color | Background color

#### Attributes

Name  | Occ    | Type                  | Description       | Default
----- | ------ | --------------------- | ----------------- | -------
prst  | [0..1] | a:ST_PresetPatternVal | Preset Pattern    | 

#### Schema

```
<xsd:complexType name="CT_PatternFillProperties">
  <xsd:sequence>
    <xsd:element name="fgClr" type="CT_Color" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="bgClr" type="CT_Color" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="prst" type="ST_PresetPatternVal" use="optional"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_pattFill-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.patternfill.aspx
