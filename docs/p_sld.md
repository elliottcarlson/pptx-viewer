# &lt;p:sld&gt;

Presentation Slide

#### Description

This element specifies the existence of a single shape. A shape can either be a preset or a custom geometry, defined using the DrawingML framework. In addition to a geometry each shape can have both visual and non-visual properties attached. Text and corresponding styling information can also be attached to a shape. This shape is specified along with all other shapes within either the shape tree or group shape elements.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_Slide

#### Parent Elements

Root element of PresentationML Slide part.

#### Child Elements

Name         | Occ    | Type                      | Description
------------ | ------ | ------------------------- | ----------------------------
p:cSld       | [1..1] | p:CT_CommonSlideData      | Common slide data for slides
a:clsMapOvr  | [0..1] | a:CT_ColorMappingOverride | Color Scheme Map Override
p:transition | [0..1] | p:CT_SlideTransition      | Slide Transition
p:timing     | [0..1] | p:CT_SlideTiming          | Slide Timing Information
p:extLst     | [0..1] | p:CT_ExtensionListModify  | Extension List with Mod Flag

#### Attributes

Name             | Occ    | Type        | Description                        | Default
---------------- | ------ | ----------- | ---------------------------------- | -------
showMasterSp     | [0..1] | xsd:boolean | Show Master Shapes                 | "true"
showMasterPhAnin | [0..1] | xsd:boolean | Show Master Placeholder Animations | "true"
show             | [0..1] | xsd:boolean | Show Slide in Slide Show           | "true"

#### Schema

```
<xsd:complexType name="CT_Slide">
  <xsd:sequence>
    <xsd:element name="cSld"       type="CT_CommonSlideData"/>
    <xsd:element name="clrMapOvr"  type="a:CT_ColorMappingOverride" minOccurs="0"/>
    <xsd:element name="transition" type="CT_SlideTransition"        minOccurs="0"/>
    <xsd:element name="timing"     type="CT_SlideTiming"            minOccurs="0"/>
    <xsd:element name="extLst"     type="CT_ExtensionListModify"    minOccurs="0"/>
  </xsd:sequence>
  <xsd:attribute name="showMasterSp"     type="xsd:boolean" default="true"/>
  <xsd:attribute name="showMasterPhAnim" type="xsd:boolean" default="true"/>
  <xsd:attribute name="show"             type="xsd:boolean" default="true"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_sld.html
http://python-pptx.readthedocs.org/en/develop/dev/analysis/schema/ct_slide.html
https://msdn.microsoft.com/en-us/library/documentformat.openxml.presentation.slide(v=office.15).aspx
