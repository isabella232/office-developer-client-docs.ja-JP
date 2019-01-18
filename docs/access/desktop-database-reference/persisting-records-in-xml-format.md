---
title: XML 形式でのレコードの永続化
TOCTitle: Persisting records in XML format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 10a5651c74580950810211c4f71e19fc80a16a95
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714725"
---
# <a name="persisting-records-in-xml-format"></a>XML 形式でのレコードの永続化

**適用されます**Access 2013、Office 2013。

ADTG 形式と同様に、XML 形式での **Recordset** の保存は、Microsoft OLE DB Persistence Provider で実装されます。このプロバイダーは、保存された XML ファイル、または ADO により生成されたスキーマ情報を含むストリームから前方スクロール型の読み取り専用行セットを生成します。同様に、プロバイダーは、ADO **Recordset** を取得し、XML を生成し、ファイルまたは COM **IStream** インターフェイスを実装する任意のオブジェクトに保存できます (実際には、ファイルも **IStream** をサポートするオブジェクトの一例です)。バージョン 2.5 以降の場合、ADO は Microsoft XML Parser (MSXML) に依存して XML を **Recordset** に読み込むため、msxml.dll が必要になります。バージョン 2.5 の場合、MSXML は Internet Explorer 5 に組み込まれて提供されています。バージョン 2.6 の場合、MSXML は SQL Server 2000 に組み込まれて提供されています。

> [!NOTE]
> [!メモ] 階層 **Recordset** (データ シェイプ) を XML 形式で保存する場合、いくつかの制限が適用されます。階層 **Recordset** に保留中の更新が含まれている場合、XML では保存できず、パラメーター化された階層 **Recordset** も保存することはできません。詳細については、「 [XML の階層 Recordsets](hierarchical-recordsets-in-xml.md)」を参照してください。


データを ADO を介して XML で保存し、再び読み込む最も簡単な方法は、それぞれに **Save** メソッドと **Open** メソッドを使用することです。次の ADO コードの例では、Titles テーブルのデータを titles.sav というファイルに保存します。

```vb 
 
Dim rs as new Recordset 
Dim rs2 as new Recordset 
Dim c as new Connection 
Dim s as new Stream 
 
' Query the Titles table. 
c.Open "provider='sqloledb';data source='mydb';initial catalog='pubs';Integrated Security='SSPI'" 
rs.cursorlocation = adUseClient 
rs.Open "select * from titles", c, adOpenStatic 
 
' Save to the file in the XML format. Note that if you don't specify 
' adPersistXML, a binary format (ADTG) will be used by default. 
rs.Save "titles.sav", adPersistXML 
 
' Save the Recordset into the ADO Stream object. 
rs.save s, adPersistXML 
rs.Close 
c.Close 
 
set rs = nothing 
 
Reopen the file. 
rs.Open "titles.sav",,,,adCmdFile 
'Open the Stream back into a Recordset. 
rs2.open s 
```

ADO では、常に **Recordset** オブジェクト全体が保存されます。 **Recordset** オブジェクトの行のサブセットのみを保存する場合は、 **Filter** メソッドを使用して行を限定するか、または選択句を変更します。 ただし、クライアント側カーソルで**Recordset**オブジェクトを開く必要があります (**CursorLocation** = **adUseClient**) メソッドを使用して、**フィルター**の行のサブセットを保存します。 たとえば、文字 "b" で始まるタイトルを取得するには、開いている **Recordset** オブジェクトに次のフィルターを適用します。

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO では、常に Client Cursor Engine 行セットを使用して、Persistence Provider によって生成された前方スクロール型のデータに基づき、スクロール可能でブックマークを指定できる **Recordset** オブジェクトを作成します。

このセクションには、次のトピックが含まれています。

- [XML の保存形式](xml-persistence-format.md)

- [名前空間](namespaces.md)

- [Schema セクション](schema-section.md)

- [データ セクション](data-section.md)

- [XML の階層 Recordset](hierarchical-recordsets-in-xml.md)

- [XML のレコードセットの動的プロパティ](recordset-dynamic-properties-in-xml.md)

- [XSLT 変換](xslt-transformations.md)

- [XML DOM オブジェクトに保存する](saving-to-the-xml-dom-object.md)

- [XML のセキュリティに関する考慮事項](xml-security-considerations.md)

- [XML Recordset を保存するシナリオのトピック](xml-recordset-persistence-scenario.md)
