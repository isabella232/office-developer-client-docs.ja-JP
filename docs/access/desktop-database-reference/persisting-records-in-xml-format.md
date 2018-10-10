---
title: レコードを XML 形式で保存する
TOCTitle: Persisting Records in XML Format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b1e22c3f85c4289520326c34c6d0c218a442a3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478062"
---
# <a name="persisting-records-in-xml-format"></a>レコードを XML 形式で保存する


**適用されます**Access 2013 |。Office 2013

ADTG 形式と同様に、XML 形式での **Recordset** の保存は、Microsoft OLE DB Persistence Provider で実装されます。このプロバイダーは、保存された XML ファイル、または ADO により生成されたスキーマ情報を含むストリームから前方スクロール型の読み取り専用行セットを生成します。同様に、プロバイダーは、ADO **Recordset** を取得し、XML を生成し、ファイルまたは COM **IStream** インターフェイスを実装する任意のオブジェクトに保存できます (実際には、ファイルも **IStream** をサポートするオブジェクトの一例です)。バージョン 2.5 以降の場合、ADO は Microsoft XML Parser (MSXML) に依存して XML を **Recordset** に読み込むため、msxml.dll が必要になります。バージョン 2.5 の場合、MSXML は Internet Explorer 5 に組み込まれて提供されています。バージョン 2.6 の場合、MSXML は SQL Server 2000 に組み込まれて提供されています。


> [!NOTE]
> <P>[!メモ] 階層 <STRONG>Recordset</STRONG> (データ シェイプ) を XML 形式で保存する場合、いくつかの制限が適用されます。階層 <STRONG>Recordset</STRONG> に保留中の更新が含まれている場合、XML では保存できず、パラメーター化された階層 <STRONG>Recordset</STRONG> も保存することはできません。詳細については、「 <A href="hierarchical-recordsets-in-xml.md">XML の階層 Recordsets</A>」を参照してください。</P>



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

