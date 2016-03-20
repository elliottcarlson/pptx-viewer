# &lt;p:spPr&gt;

Shape Properties

#### Description

This element specifies the properties for a single shape in a diagram's data, as defined using DrawingML child elements.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: a:CT_ShapeProperties

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:cxnSp            | p:CT_Connector
p:pic              | p:CT_Picture
p:sp               | p:CT_Shape

#### Child Elements

Name        | Occ    | Type                          | Description
----------- | ------ | ----------------------------- | ----------------------------
a:xfrm      | [0..1] | a:CT_Transform2D              | 2D Transform for Individual Objects
a:custGeom  | [0..1] | a:CT_CustomGeometry2D         | Custom Geometry
a:prstGeom  | [0..1] | a:CT_PresetGeometry2D         | Preset Geometry
a:noFill    | [0..1] | a:CT_NoFillProperties         | No Fill
a:solidFill | [0..1] | a:CT_SolidColorFillProperties | Solid Fill
a:gradFill  | [0..1] | a:CT_GradientFillProperties   | Gradient Fill
a:blipFill  | [0..1] | a:CT_BlipFillProperties       | Picture Fill
a:pattFill  | [0..1] | a:CT_PatternFillProperties    | Pattern Fill
a:grpFill   | [0..1] | a:CT_GroupFillProperties      | Group Fill
a:ln        | [0..1] | a:CT_LineProperties           | Outlin Properties
a:effectLst | [0..1] | a:CT_EffectList               | Effect Container
a:effectDag | [0..1] | a:CT_EffectContainer          | Effect Container
a:scene3d   | [0..1] | a:CT_Scene3D                  | 3-D Scene
a:sp3d      | [0..1] | a:CT_Shape3D                  | 3-D Shape Properties
a:extLst    | [0..1] | a:CT_OfficeArtExtensionList   | Extension List

#### Attributes

Name   | Occ    | Type                | Description          | Default
------ | ------ | ------------------- | -------------------- | -------
bwMode | [0..1] | a:ST_BlackWhiteMode | Black and White Mode | 

#### Schema

```
<xsd:complexType name="CT_LineProperties">
  <xsd:sequence>
    <xsd:group ref="EG_LineFillProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="EG_LineDashProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="EG_LineJoinProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="headEnd" type="CT_LineEndProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="tailEnd" type="CT_LineEndProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_OfficeArtExtensionList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="w" type="ST_LineWidth" use="optional"/>
  <xsd:attribute name="cap" type="ST_LineCap" use="optional"/>
  <xsd:attribute name="cmpd" type="ST_CompoundLine" use="optional"/>
  <xsd:attribute name="algn" type="ST_PenAlignment" use="optional"/>
</xsd:complexType>

<xsd:group name="EG_LineFillProperties">
  <xsd:choice>
    <xsd:element name="noFill" type="CT_NoFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="solidFill" type="CT_SolidColorFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="gradFill" type="CT_GradientFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="pattFill" type="CT_PatternFillProperties" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>

<xsd:group name="EG_LineDashProperties">
  <xsd:choice>
    <xsd:element name="prstDash" type="CT_PresetLineDashProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="custDash" type="CT_DashStopList" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>

<xsd:group name="EG_LineJoinProperties">
  <xsd:choice>
    <xsd:element name="round" type="CT_LineJoinRound" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="bevel" type="CT_LineJoinBevel" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="miter" type="CT_LineJoinMiterProperties" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_spPr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.diagrams.shapeproperties.aspx
