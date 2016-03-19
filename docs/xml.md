# &lt;?xml&gt;

XML Declaration

#### Description

The XML declaration is a processing instruction that identifies the document as being XML. All XML documents should begin with an XML declaration.

#### Parent/Child Elements

The XML declaration is not a standard element and thus has no parents or children. If it exists, it must be the first line in an XML file. The XML declaration has no closing tag, that is `</?xml>`.

#### Attributes

Name       | Occ    | Type        | Description                     | Default
---------- | ------ | ----------- | ------------------------------- | -------
version    | [1..1] | xsd:integer | Version of XML Standard in use  | 
encoding   | [0..1] | xsd:string  | Document character set encoding | "UTF-8"
standalone | [0..1] | xsd:string  | Use a internal or external DTD  | "no"

#### References

https://xmlwriter.net/xml_guide/xml_declaration.shtml
