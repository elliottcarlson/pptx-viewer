# &lt;a:blipFill&gt;

Picture Fill

#### Description

This element specifies the kind of picture fill that the picture object has. Because a picture has a picture fill already by default, it is possible to have two fills specified for a picture object. An example of this is shown below.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_BlipFillProperties

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
a:blip      | [0..1] | a:CT_Blip                  | Blip
a:srcRect   | [0..1] | a:CT_RelativeRect          | Source Rectangle
a:tile      | [0..1] | a:CT_TileInfoProperties    | Tile
a:stretch   | [0..1] | a:CT_StretchInfoProperties | Stretch

#### Attributes

Name         | Occ    | Type              | Description       | Default
------------ | ------ | ----------------- | ----------------- | -------
dpi          | [0..1] | xsd:unsignedint   | DPI Setting       | 
rotWithShape | [0..1] | xsd:boolean       | Rotate With Shape | 

#### Schema

```
<xsd:complexType name="CT_BlipFillProperties">
  <xsd:sequence>
    <xsd:element name="blip" type="CT_Blip" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="srcRect" type="CT_RelativeRect" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="EG_FillModeProperties" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="dpi" type="xsd:unsignedInt" use="optional"/>
  <xsd:attribute name="rotWithShape" type="xsd:boolean" use="optional"/>
</xsd:complexType>

<xsd:group name="EG_FillModeProperties">
  <xsd:choice>
    <xsd:element name="tile" type="CT_TileInfoProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="stretch" type="CT_StretchInfoProperties" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_blipFill-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.presentation.blipfill.aspx
