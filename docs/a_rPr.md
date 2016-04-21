# &lt;a:rPr&gt;

Text Character Properties

#### Description

This element contains all run level text properties for the text runs within a containing paragraph.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_TextCharacterProperties

#### Parent Elements

Name  | Type
----- | ------------------
a:fld | a:CT_TextField
a:r   | a:CT_RegularTextRun

#### Child Elements

Name             | Occ    | Type                               | Description
---------------- | ------ | ---------------------------------- | ----------------------------
a:ln             | [0..1] | a:CT_LineProperties                | Line
a:noFill         | [0..1] | a:CT_NoFillProperties              | No Fill
a:solidFill      | [0..1] | a:CT_SolidColorFillProperties      | Solid Fill
a:gradFill       | [0..1] | a:CT_GradientFillProperties        | Gradient Fill
a:blipFill       | [0..1] | a:CT_BlipFillProperties            | Picture Fill
a:pattFill       | [0..1] | a:CT_PatternFillProperties         | Pattern Fill
a:grpFill        | [0..1] | a:CT_GroupFillProperties           | Group Fill
a:effectLst      | [0..1] | a:CT_EffectList                    | Effect Container
a:effectDag      | [0..1] | a:CT_EffectContainer               | Effect Container
a:highlight      | [0..1] | a:CT_Color                         | Highlight Color
a:uLnTx          | [0..1] | a:CT_TextUnderlineLineFollowText   | Underline Follows Text
a:uLn            | [0..1] | a:CT_LineProperties                | Underline Stroke
a:uFillTx        | [0..1] | a:CT_TextUnderlineFillFollowText   | Underline Fill Properties Follow Text
a:uFill          | [0..1] | a:CT_TextUnderlineFillGroupWrapper | Underline Fill
a:latin          | [0..1] | a:CT_TextFont                      | Latin Font
a:ea             | [0..1] | a:CT_TextFont                      | East Asian Font
a:cs             | [0..1] | a:CT_TextFont                      | Complext Script Font
a:sym            | [0..1] | a:CT_TextFont                      | Symbol Font
a:hlinkClick     | [0..1] | a:CT_Hyperlink                     | Click Hyperlink
a:hlinkMouseOver | [0..1] | a:CT_Hyperlink                     | Mouse-Over Hyperlink
a:extLst         | [0..1] | a:CT_OfficeArtExtensionList        | Extension List

#### Attributes

Name       | Occ    | Type                      | Description           | Default
---------- | ------ | ------------------------- | --------------------- | -------
kumimoji   | [0..1] | xsd:boolean               | Kumimoji              | 
lang       | [0..1] | a:ST_TextLanguageID       | Language ID           | 
altLang    | [0..1] | a:ST_TextLanguageID       | Alternative Language  | 
sz         | [0..1] | a:ST_TextFontSize         | Font Size             | 
b          | [0..1] | xsd:boolean               | Bold                  | 
i          | [0..1] | xsd:boolean               | Italics               | 
u          | [0..1] | a:ST_TextUnderlineType    | Underline             | 
strike     | [0..1] | a:ST_TextStrikeType       | Strikethrough         | 
kern       | [0..1] | a:ST_TextNonNegativePoint | Kerning               | 
cap        | [0..1] | a:ST_TextCapsType         | Capitalization        | 
spc        | [0..1] | a:ST_TextPoint            | Spacing               | 
normalizeH | [0..1] | xsd:boolean               | Normalize Heights     | 
baseline   | [0..1] | a:ST_Percentage           | Baseline              | 
noProof    | [0..1] | xsd:boolean               | No Proofing           | 
dirty      | [0..1] | xsd:boolean               | Dirty                 | "true"
err        | [0..1] | xsd:boolean               | Spelling Error        | "false"
smtClean   | [0..1] | xsd:boolean               | SmartTag Clean        | "true"
smtId      | [0..1] | xsd:unsignedInt           | SmartTag ID           | "0"
bmk        | [0..1] | xsd:string                | Bookmark Link Target  | 

#### Schema

```
<xsd:complexType name="CT_TextCharacterProperties">
  <xsd:sequence>
    <xsd:element name="ln"             type="CT_LineProperties" minOccurs="0"/>
    <xsd:group   ref="EG_FillProperties"                        minOccurs="0"/>
    <xsd:group   ref="EG_EffectProperties"                      minOccurs="0"/>
    <xsd:element name="highlight"      type="CT_Color"          minOccurs="0"/>
    <xsd:group   ref="EG_TextUnderlineLine"                     minOccurs="0"/>
    <xsd:group   ref="EG_TextUnderlineFill"                     minOccurs="0"/>
    <xsd:element name="latin"          type="CT_TextFont"       minOccurs="0"/>
    <xsd:element name="ea"             type="CT_TextFont"       minOccurs="0"/>
    <xsd:element name="cs"             type="CT_TextFont"       minOccurs="0"/>
    <xsd:element name="sym"            type="CT_TextFont"       minOccurs="0"/>
    <xsd:element name="hlinkClick"     type="CT_Hyperlink"      minOccurs="0"/>
    <xsd:element name="hlinkMouseOver" type="CT_Hyperlink"      minOccurs="0"/>
    <xsd:element name="rtl"            type="CT_Boolean"        minOccurs="0"/>
    <xsd:element name="extLst"         type="CT_OfficeArtExtensionList" minOccurs="0" />
  </xsd:sequence>
  <xsd:attribute name="kumimoji"   type="xsd:boolean"/>
  <xsd:attribute name="lang"       type="s:ST_Lang"/>
  <xsd:attribute name="altLang"    type="s:ST_Lang"/>
  <xsd:attribute name="sz"         type="ST_TextFontSize"/>
  <xsd:attribute name="b"          type="xsd:boolean"/>
  <xsd:attribute name="i"          type="xsd:boolean"/>
  <xsd:attribute name="u"          type="ST_TextUnderlineType"/>
  <xsd:attribute name="strike"     type="ST_TextStrikeType"/>
  <xsd:attribute name="kern"       type="ST_TextNonNegativePoint"/>
  <xsd:attribute name="cap"        type="ST_TextCapsType"/>
  <xsd:attribute name="spc"        type="ST_TextPoint"/>
  <xsd:attribute name="normalizeH" type="xsd:boolean"/>
  <xsd:attribute name="baseline"   type="ST_Percentage"/>
  <xsd:attribute name="noProof"    type="xsd:boolean"/>
  <xsd:attribute name="dirty"      type="xsd:boolean"     default="true"/>
  <xsd:attribute name="err"        type="xsd:boolean"     default="false"/>
  <xsd:attribute name="smtClean"   type="xsd:boolean"     default="true"/>
  <xsd:attribute name="smtId"      type="xsd:unsignedInt" default="0"/>
  <xsd:attribute name="bmk"        type="xsd:string"/>
</xsd:complexType>

<xsd:simpleType name="ST_TextUnderlineType">
  <xsd:restriction base="xsd:token">
    <xsd:enumeration value="none"/>
    <xsd:enumeration value="words"/>
    <xsd:enumeration value="sng"/>
    <xsd:enumeration value="dbl"/>
    <xsd:enumeration value="heavy"/>
    <xsd:enumeration value="dotted"/>
    <xsd:enumeration value="dottedHeavy"/>
    <xsd:enumeration value="dash"/>
    <xsd:enumeration value="dashHeavy"/>
    <xsd:enumeration value="dashLong"/>
    <xsd:enumeration value="dashLongHeavy"/>
    <xsd:enumeration value="dotDash"/>
    <xsd:enumeration value="dotDashHeavy"/>
    <xsd:enumeration value="dotDotDash"/>
    <xsd:enumeration value="dotDotDashHeavy"/>
    <xsd:enumeration value="wavy"/>
    <xsd:enumeration value="wavyHeavy"/>
    <xsd:enumeration value="wavyDbl"/>
  </xsd:restriction>

<xsd:group name="EG_TextUnderlineLine">
  <xsd:choice>
    <xsd:element name="uLnTx" type="CT_TextUnderlineLineFollowText"/>
    <xsd:element name="uLn"   type="CT_LineProperties" minOccurs="0"/>
  </xsd:choice>
</xsd:group>

<xsd:group name="EG_TextUnderlineFill">
  <xsd:choice>
    <xsd:element name="uFillTx" type="CT_TextUnderlineFillFollowText"/>
    <xsd:element name="uFill"   type="CT_TextUnderlineFillGroupWrapper"/>
  </xsd:choice>
</xsd:group>

<xsd:complexType name="CT_TextUnderlineLineFollowText"/>

<xsd:complexType name="CT_TextUnderlineFillFollowText"/>

<xsd:complexType name="CT_TextUnderlineFillGroupWrapper">
  <xsd:group ref="EG_FillProperties"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_rPr-2.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.runproperties.aspx
http://python-pptx.readthedocs.org/en/latest/dev/analysis/features/txt-font-typeface.html
http://python-pptx.readthedocs.org/en/latest/dev/analysis/features/txt-font-color.html
http://python-pptx.readthedocs.org/en/latest/dev/analysis/features/txt-font-underline.html
