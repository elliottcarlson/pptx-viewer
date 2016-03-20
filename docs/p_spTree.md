# &lt;p:spTree&gt;

Shape Tree

#### Description

This complex type specifies a group shape that represents one or more shapes grouped together. This shape is to be treated as if it were a regular shape, but instead of being described by a single geometry, it is made up of all the shape geometries encompassed within it. Within a group shape, each shape in the group is specified as it normally would be. However, a single transform can apply to the group of shapes as though it were a single shape.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_GroupShape

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:cSld             | p:CT_CommonSlideData

#### Child Elements

Name           | Occ    | Type                      | Description
-------------- | ------ | ------------------------- | ----------------------------
p:nvGrpSpPr    | [1..1] | p:CT_GroupShapeNonVisual  | Non-Visual Properties for a Group Shape
a:grpSpPr      | [1..1] | p:CT_GroupShapeProperties | Group Shape Properties
p:sp           | [0..*] | p:CT_Shape                | Shape
p:grpSp        | [0..*] | p:CT_GroupShape           | Group Shape
p:graphicFrame | [0..*] | p:CT_GraphicalObjectFrame | Graphic Frame
p:cxnSp        | [0..*] | p:CT_Connector            | Connection Shape
p:pic          | [0..*] | p:CT_Picture              | Picture
p:extLst       | [0..1] | p:CT_ExtensionListModify  | Extension List with Modification Flag

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_GroupShape">
  <xsd:sequence>
    <xsd:element name="nvGrpSpPr" type="CT_GroupShapeNonVisual" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="grpSpPr" type="a:CT_GroupShapeProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:choice minOccurs="0" maxOccurs="unbounded">
      <xsd:element name="sp" type="CT_Shape"/>
      <xsd:element name="grpSp" type="CT_GroupShape"/>
      <xsd:element name="graphicFrame" type="CT_GraphicFrame"/>
      <xsd:element name="cxnSp" type="CT_Connector"/>
      <xsd:element name="pic" type="CT_Picture"/>
    </xsd:choice>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_spTree-1.html
