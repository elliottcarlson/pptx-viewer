# &lt;a:avLst&gt;

Adjust Value List

#### Description

This element specifies the adjust values that are applied to the specified shape. An adjust value is simply a guide that has a value based formula specified. That is, no calculation takes place for an adjust value guide. Instead, this guide specifies a parameter value that is used for calculations within the shape guides.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_GeomGuideList

#### Parent Elements

Name             | Type
---------------- | ----------------------------------
a:custGeom       | a:CT_CustomGeometry2D
a:prstTxWarp     | a:CT_PresetTextShape

#### Child Elements

Name     | Occ    | Type           | Description
-------- | ------ | -------------- | -------------
a:gd     | [0..*] | a:CT_GeomGuide | Shape Guide

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_GeomGuideList">
  <xsd:sequence>
    <xsd:element name="gd" type="CT_GeomGuide" minOccurs="0" maxOccurs="unbounded"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_avLst-2.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.adjustvaluelist.aspx
