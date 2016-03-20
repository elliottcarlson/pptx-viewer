# &lt;a:scrgbClr&gt;

RGB Color Model - Percentage Variant

#### Description

s element specifies a color using the red, green, blue color model. Each component, red, green, and blue is expressed as a percentage from 0% to 100%. A linear gamma of 1.0 is assumed.

Specifies the level of red as expressed by a percentage offset increase or decrease relative to the input color.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_ScRgbColor

#### Parent Elements

Name                     | Type
------------------------ | ---------------------------------
n/a                      | a:EG_ColorChoice
a:alphaInv               | a:CT_AlphaInverseEffect
p:clrMru                 | a:CT_ColorMRU
a:clrRepl                | a:CT_ColorReplaceEffect
a:custClr                | a:CT_CustomColor
a:duotone                | a:CT_DuotoneEffect
a:fontRef                | a:CT_FontReference
a:glow                   | a:CT_GlowEffect
a:gs                     | a:CT_GradientStop
a:innerShdw              | a:CT_InnerShadowEffect
a:outerShdw              | a:CT_OuterShadowEffect
a:prstShdw               | a:CT_PresetShadowEffect
a:solidFill              | a:CT_SolidColorFillProperties
a:tcTxStyle              | a:CT_TableStyleTextStyle
a:lnRef                  | a:CT_StyleMatrixReference
a:fillRef                | a:CT_StyleMatrixReference
a:effectRef              | a:CT_StyleMatrixReference
p:bgRef                  | a:CT_StyleMatrixReference
draw-diag:fillClrLst     | draw-diag:CT_Colors
draw-diag:linClrLst      | draw-diag:CT_Colors
draw-diag:effectClrLst   | draw-diag:CT_Colors
draw-diag:txLinClrLst    | draw-diag:CT_Colors
draw-diag:txFillClrLst   | draw-diag:CT_Colors
draw-diag:txEffectClrLst | draw-diag:CT_Colors
a:dk1                    | a:CT_Color
a:lt1                    | a:CT_Color
a:dk2                    | a:CT_Color
a:lt2                    | a:CT_Color
a:accent1                | a:CT_Color
a:accent2                | a:CT_Color
a:accent3                | a:CT_Color
a:accent4                | a:CT_Color
a:accent5                | a:CT_Color
a:accent6                | a:CT_Color
a:hlink                  | a:CT_Color
a:folHlink               | a:CT_Color
a:extrusionClr           | a:CT_Color
a:contourClr             | a:CT_Color
a:clrFrom                | a:CT_Color
a:clrTo                  | a:CT_Color
a:fgClr                  | a:CT_Color
a:bgClr                  | a:CT_Color
a:buClr                  | a:CT_Color
a:highlight              | a:CT_Color
p:clrVal                 | a:CT_Color
p:from                   | a:CT_Color
p:to                     | a:CT_Color
p:penClr                 | a:CT_Color

#### Child Elements

Name       | Occ    | Type                         | Description
---------- | ------ | ---------------------------- | ---------------------
a:tint     | [0..*] | a:CT_PositiveFixedPercentage | Tint
a:shade    | [0..*] | a:CT_PositiveFixedPercentage | Shade
a:comp     | [0..*] | a:CT_ComplementTransform     | Complement
a:inv      | [0..*] | a:CT_InverseTransform        | Inverse
a:gray     | [0..*] | a:CT_GrayscaleTransform      | Gray
a:alpha    | [0..*] | a:CT_PositiveFixedPercentage | Alpha
a:alphaOff | [0..*] | a:CT_FixedPercentage         | Alpha Offset
a:alphaMod | [0..*] | a:CT_PositivePercentage      | Alpha Modulation
a:hue      | [0..*] | a:CT_PositiveFixedAngle      | Hue
a:hueOff   | [0..*] | a:CT_Angle                   | Hue Offset
a:hueMod   | [0..*] | a:CT_PositivePercentage      | Hue Modulate
a:sat      | [0..*] | a:CT_Percentage              | Saturation
a:satOff   | [0..*] | a:CT_Percentage              | Saturation Offset
a:satMod   | [0..*] | a:CT_Percentage              | Saturation Modulation
a:lum      | [0..*] | a:CT_Percentage              | Luminance
a:lumOff   | [0..*] | a:CT_Percentage              | Luminance Offset
a:lumMod   | [0..*] | a:CT_Percentage              | Luminance Modulation
a:red      | [0..*] | a:CT_Percentage              | Red
a:redOff   | [0..*] | a:CT_Percentage              | Red Offset
a:redMod   | [0..*] | a:CT_Percentage              | Red Modulation
a:green    | [0..*] | a:CT_Percentage              | Green
a:greenOff | [0..*] | a:CT_Percentage              | Green Offset
a:greenMod | [0..*] | a:CT_Percentage              | Green Modification
a:blue     | [0..*] | a:CT_Percentage              | Blue
a:blueOff  | [0..*] | a:CT_Percentage              | Blue Offset
a:blueMod  | [0..*] | a:CT_Percentage              | Blue Modification
a:gamma    | [0..*] | a:CT_GammaTransform          | Gamma
a:invGamma | [0..*] | a:CT_InverseGammaTransform   | Inverse Gamma

#### Attributes

Name      | Occ    | Type            | Description    | Default
--------- | ------ | --------------- | -------------- | -------
r         | [1..1] | a:ST_Percentage | Red            | 
g         | [1..1] | a:ST_Percentage | Green          | 
b         | [1..1] | a:ST_Percentage | Blue           | 

#### Schema

```
<xsd:complexType name="CT_ScRgbColor">
  <xsd:sequence>
    <xsd:group ref="EG_ColorTransform" minOccurs="0" maxOccurs="unbounded"/>
  </xsd:sequence>
  <xsd:attribute name="r" type="ST_Percentage" use="required"/>
  <xsd:attribute name="g" type="ST_Percentage" use="required"/>
  <xsd:attribute name="b" type="ST_Percentage" use="required"/>
</xsd:complexType>

<xsd:group name="EG_ColorTransform">
  <xsd:choice>
    <xsd:element name="tint" type="CT_PositiveFixedPercentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="shade" type="CT_PositiveFixedPercentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="comp" type="CT_ComplementTransform" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="inv" type="CT_InverseTransform" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="gray" type="CT_GrayscaleTransform" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="alpha" type="CT_PositiveFixedPercentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="alphaOff" type="CT_FixedPercentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="alphaMod" type="CT_PositivePercentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="hue" type="CT_PositiveFixedAngle" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="hueOff" type="CT_Angle" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="hueMod" type="CT_PositivePercentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="sat" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="satOff" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="satMod" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="lum" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="lumOff" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="lumMod" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="red" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="redOff" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="redMod" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="green" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="greenOff" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="greenMod" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="blue" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="blueOff" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="blueMod" type="CT_Percentage" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="gamma" type="CT_GammaTransform" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="invGamma" type="CT_InverseGammaTransform" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_scrgbClr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.rgbcolormodelpercentage.aspx
