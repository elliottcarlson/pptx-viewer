# &lt;p:cNvSpPr&gt;

Non-Visual Drawing Properties for a Shape

#### Description

This element specifies the non-visual drawing properties for a shape. These properties are to be used by the generating application to determine how the shape should be dealt with.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: a:CT_NonVisualDrawingShapeProps

#### Parent Elements

Name     | Type
-------- | -------------------
p:nvSpPr | p:CT_ShapeNonVisual

#### Child Elements

Name      | Occ    | Type                        | Description
--------- | ------ | --------------------------- | --------------
a:spLocks | [0..1] | a:CT_ShapeLocking           | Shape Locks
a:extLst  | [0..1] | a:CT_OfficeArtExtensionList | Extension List

#### Attributes

Name      | Occ    | Type        | Description         | Default
--------- | ------ | ----------- | ------------------- | -------
txBox     | [0..1] | xsd:boolean | Text Box            | "false"

#### Schema

```
<xsd:complexType name="CT_NonVisualDrawingShapeProps">
  <xsd:sequence>
    <xsd:element name="spLocks" type="CT_ShapeLocking" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_OfficeArtExtensionList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="txBox" type="xsd:boolean" use="optional" default="false"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_cNvSpPr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.chartdrawing.nonvisualshapedrawingproperties.aspx
