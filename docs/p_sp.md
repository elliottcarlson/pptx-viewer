# &lt;p:sp&gt;

Shape

#### Description

This element specifies the existence of a single shape. A shape can use either a preset or a custom geometry, defined by using the DrawingML framework. In addition to a geometry, each shape can have both visual and non-visual properties. Text and corresponding styling information can also be attached to a shape. This shape is specified along with all other shapes in group shape elements.


#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_Shape

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:grpSp            | p:CT_GroupShape
p:spTree           | p:CT_GroupShape

#### Child Elements

Name     | Occ    | Type                     | Description
-------- | ------ | ------------------------ | ----------------------------
p:nvSpPr | [1..1] | p:CT_ShapeNonVisual      | Non-Visual Properties for a Shape
p:spPr   | [1..1] | a:CT_ShapeProperties     | Shape Properties
p:style  | [0..1] | a:CT_ShapeStyle          | Shape Style
p:txBody | [0..1] | a:CT_TextBody            | Shape Text Body
p.extLst | [0..1] | p:CT_ExtensionListModify | Extension List with Modification Flag

#### Attributes

Name      | Occ    | Type        | Description         | Default
--------- | ------ | ----------- | ------------------- | -------
useBgFill | [0..1] | xsd:boolean | Use Background Fill | "false"

#### Schema

```
<xsd:complexType name="CT_Shape">
  <xsd:sequence>
    <xsd:element name="nvSpPr" type="CT_ShapeNonVisual" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="spPr" type="a:CT_ShapeProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="style" type="a:CT_ShapeStyle" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="txBody" type="a:CT_TextBody" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_ExtensionListModify" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="useBgFill" type="xsd:boolean" use="optional"
default="false"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_sp-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.office.drawing.shape.aspx
