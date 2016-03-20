# &lt;p:ph&gt;

Placeholder Shape

#### Description

This element specifies that the corresponding shape should be represented by the generating application as a placeholder. When a shape is considered a placeholder by the generating application it can have special properties to alert the user that they can enter content into the shape. Different placeholder types are allowed and can be specified by using the placeholder type attribute for this element.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_Placeholder

#### Parent Elements

Name               | Type
------------------ | -------------------------------------
p:nvPr             | p:CT_ApplicationNonVisualDrawingProps

#### Child Elements

Name     | Occ    | Type                     | Description
-------- | ------ | ------------------------ | -------------------------------------
p.extLst | [0..1] | p:CT_ExtensionListModify | Extension List with Modification Flag

#### Attributes

Name            | Occ    | Type                 | Description                   | Default
--------------- | ------ | -------------------- | ----------------------------- | -------
type            | [0..1] | p:ST_PlaceholderType | Placeholder Type              | "obj"
orient          | [0..1] | p:ST_Direction       | Placeholder Orientation       | "horz"
sz              | [0..1] | p:ST_PlaceholderSize | Placeholder Size              | "full"
idx             | [0..1] | xsd:unsignedint      | Placeholder Index             | "0"
hasCustomPrompt | [0..1] | xsd:boolean          | Placeholder has custom prompt | "false"

#### Schema

```
<xsd:complexType name="CT_Placeholder">
  <xsd:sequence>
    <xsd:element name="extLst" type="CT_ExtensionListModify" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="type" type="ST_PlaceholderType" use="optional" default="obj"/>
  <xsd:attribute name="orient" type="ST_Direction" use="optional" default="horz"/>
  <xsd:attribute name="sz" type="ST_PlaceholderSize" use="optional" default="full"/>
  <xsd:attribute name="idx" type="xsd:unsignedInt" use="optional" default="0"/>
  <xsd:attribute name="hasCustomPrompt" type="xsd:boolean" use="optional" default="false"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_ph-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.presentation.placeholdershape.aspx
