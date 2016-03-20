# &lt;p:cNvPr&gt;

Non-Visual Drawing Properties

#### Description

This element specifies non-visual canvas properties. This allows for additional information that does not affect the appearance of the picture to be stored.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: a:CT_NonVisualDrawingProps

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:nvCxnSoPr        | p:CT_ConnectorNonVisual
p:nvGraphicFramePr | p:CT_GraphicalObjectFrameNonVisual
p:nvGrpSpPr        | p:CT_GroupShapeNonVisual
p:nvPicPr          | p:CT_PictureNonVisual
p:nvSpPr           | p:CT_ShapeNonVisual

#### Child Elements

Name         | Occ    | Type                        | Description
------------ | ------ | --------------------------- | ----------------------------
a:hlinkClick | [0..1] | a:CT_Hyperlink              | Drawing Element On Click Hyperlink
a:hlinkHover | [0..1] | a:CT_Hyperlink              | Hyperlink for Hover
a:extLst     | [0..1] | a:CT_OfficeArtExtensionList | Extension List

#### Attributes

Name   | Occ    | Type                  | Description                 | Default
------ | ------ | --------------------- | --------------------------- | -------
id     | [1..1] | a:ST_DrawingElementId | Unique Identifier           |
name   | [1..1] | xsd:string            | Name                        |
descr  | [0..1] | xsd:string            | Alternative Text for Object | ""
title  | [0..1] | xsd:string            | Undocument besides in XSD   | ""
hidden | [0..1] | xsd:boolean           | Visual state                | "false"

#### Schema

```
<xsd:complexType name="CT_NonVisualDrawingProps">
  <xsd:sequence>
    <xsd:element name="hlinkClick" type="CT_Hyperlink" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="hlinkHover" type="CT_Hyperlink" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_OfficeArtExtensionList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="id" type="ST_DrawingElementId" use="required"/>
  <xsd:attribute name="name" type="xsd:string" use="required"/>
  <xsd:attribute name="descr" type="xsd:string" use="optional" default=""/>
  <xsd:attribute name="hidden" type="xsd:boolean" use="optional" default="false"/>
  <xsd:attribute name="title" type="xsd:string" use="optional" default=""/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_cNvPr-1.html
https://msdn.microsoft.com/en-us/library/documentformat.openxml.presentation.nonvisualdrawingproperties(v=office.15).aspx
