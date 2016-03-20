# &lt;p:clrMapOvr&gt;

Color Scheme Map Override

#### Description

This element provides a mechanism with which to override the color schemes listed within the ClrMap element. If the masterClrMapping element is present, the color scheme defined by the master is used. If the overrideClrMapping element is present, it defines a new color scheme specific to the parent notes slide, presentation slide, or slide layout.

#### Element information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: a:CT_ColorMappingOverride

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
n/a                | p:EG_ChildSlide
p:notes            | p:CT_NotesSlide
p:sld              | p:CT_Slide
p:sldLayout        | p:CT_SlideLayout

#### Child Elements

Name                 | Occ    | Type              | Description
-------------------- | ------ | ----------------- | ----------------------
a:masterClrMapping   | [1..1] | a:CT_EmptyElement | Master Color Mapping
a:overrideClrMapping | [1..1] | a:CT_ColorMapping | Override Color Mapping

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_ColorMappingOverride">
  <xsd:sequence>
     <xsd:choice minOccurs="1" maxOccurs="1">
      <xsd:element name="masterClrMapping" type="CT_EmptyElement"/>
      <xsd:element name="overrideClrMapping" type="CT_ColorMapping"/>
    </xsd:choice>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_overrideClrMapping-1.html
https://msdn.microsoft.com/en-us/library/documentformat.openxml.presentation.colormapoverride(v=office.15).aspx