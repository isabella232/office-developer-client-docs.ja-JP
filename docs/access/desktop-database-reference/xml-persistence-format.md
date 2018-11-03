---
title: XML の保存形式
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 291a75fb88690a5674d872f2adb01b683f5e99bd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946714"
---
# <a name="xml-persistence-format"></a>XML 永続性形式

**適用されます**Access 2013、Office 2013。

## <a name="xml-persistence-format"></a>XML の保存形式

ADO では、保存する XML ストリームに UTF-8 エンコードを使用します。

ADO XML 形式は、スキーマ セクションと、その後に続くデータ セクションの 2 つのセクションに分けられます。Northwind データベースの Shippers テーブルの XML ファイルの例を次に示します。XML のさまざまな部分について、例に続いて解説しています。

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

このスキーマには、名前空間の宣言、スキーマ セクション、およびデータ セクションが示されています。スキーマ セクションに、行、ShipperID、CompanyName、および Phone の定義が含まれています。

スキーマ定義は XML-Data の仕様に準拠し、すべて検証できます (ただし、検証は Internet Explorer 5 では行われません)。この仕様については、[W3C XML-Data ノート (英語)](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)で確認できます。XML-Data は、現在、 **Recordset** の保存をサポートしている唯一のスキーマ形式です。

データ セクションには、荷主 (Shipper) に関する情報を含む 3 つの行があります。 空の行セットのデータ セクションは空である可能性がありますが、`<rs:data>`タグが存在する必要があります。 データがない可能性がありますを記述するタグの簡単なだけで`<rs:data>`です。 プレフィックスが "rs" のタグは、urn:schemas-microsoft-com:rowset によって定義された名前空間にあることを示します。 このスキーマの完全な定義については、このドキュメントの付録を参照してください。

## <a name="xml-persistence-format"></a>XML の保存形式

ADO では、保存する XML ストリームに UTF-8 エンコードを使用します。

ADO XML 形式は、スキーマ セクションと、その後に続くデータ セクションの 2 つのセクションに分けられます。Northwind データベースの Shippers テーブルの XML ファイルの例を次に示します。XML のさまざまな部分について、例に続いて解説しています。

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

このスキーマには、名前空間の宣言、スキーマ セクション、およびデータ セクションが示されています。スキーマ セクションに、行、ShipperID、CompanyName、および Phone の定義が含まれています。

スキーマ定義は XML-Data の仕様に準拠し、すべて検証できます (ただし、検証は Internet Explorer 5 では行われません)。この仕様については、[W3C XML-Data ノート (英語)](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)で確認できます。XML-Data は、現在、 **Recordset** の保存をサポートしている唯一のスキーマ形式です。

データ セクションには、荷主 (Shipper) に関する情報を含む 3 つの行があります。 空の行セットのデータ セクションは空である可能性がありますが、`<rs:data>`タグが存在する必要があります。 データがない可能性がありますを記述するタグの簡単なだけで`<rs:data>`です。 プレフィックスが "rs" のタグは、urn:schemas-microsoft-com:rowset によって定義された名前空間にあることを示します。 このスキーマの完全な定義については、このドキュメントの付録を参照してください。

