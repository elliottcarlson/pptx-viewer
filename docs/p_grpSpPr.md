# &lt;p:grpSpPr&gt;

Group Shape Properties

#### Description

This element specifies the properties that are to be common across all of the shapes within the corresponding group. If there are any conflicting properties within the group shape properties and the individual shape properties then the individual shape properties should take precedence.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: a:CT_GroupShapeProperties

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:grpSp            | p:CT_GroupShape
p:spTree           | p:CT_GroupShape

#### Child Elements

Name        | Occ    | Type                          | Description
----------- | ------ | ----------------------------- | ----------------------------
a:xfrm      | [0..1] | a:CT_GroupTransform2D         | 2D Transform for Grouped Objects
a:noFill    | [0..1] | a:CT_NoFillProperties         | No Fill
a:solidFill | [0..1] | a:CT_SolidColorFillProperties | Solid Fill
a:gradFill  | [0..1] | a:CT_GradientFillProperties   | Gradient Fill
a:blipFill  | [0..1] | a:CT_BlipFillProperties       | Picture Fill
a:pattFill  | [0..1] | a:CT_PatternFillProperties    | Pattern Fill
a:grpFill   | [0..1] | a:CT_GroupFillProperties      | Group Fill
a:effectLst | [0..1] | a:CT_EffectList               | Effect Container
a:effectDag | [0..1] | a:CT_EffectContainer          | Effect Container
a:scene3d   | [0..1] | a:CT_Scene3D                  | 3-D Scene
a:extLst    | [0..1] | a:CT_OfficeArtExtensionList   | Extension List

#### Attributes

Name   | Occ    | Type                | Description          | Default
------ | ------ | ------------------- | -------------------- | -------
bwMode | [0..1] | a:ST_BlackWhiteMode | Black and White Mode | "false"

#### Schema

```
<xsd:complexType name="CT_GroupShapeProperties">
  <xsd:sequence>
    <xsd:element name="xfrm" type="CT_GroupTransform2D" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="EG_FillProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="EG_EffectProperties" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="scene3d" type="CT_Scene3D" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_OfficeArtExtensionList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="bwMode" type="ST_BlackWhiteMode" use="optional"/>
</xsd:complexType>

<xsd:group name="EG_FillProperties">
  <xsd:choice>
    <xsd:element name="noFill" type="CT_NoFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="solidFill" type="CT_SolidColorFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="gradFill" type="CT_GradientFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="blipFill" type="CT_BlipFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="pattFill" type="CT_PatternFillProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="grpFill" type="CT_GroupFillProperties" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>

<xsd:group name="EG_EffectProperties">
  <xsd:choice>
    <xsd:element name="effectLst" type="CT_EffectList" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="effectDag" type="CT_EffectContainer" minOccurs="1" maxOccurs="1"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_grpSpPr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.presentation.groupshapeproperties.aspx
