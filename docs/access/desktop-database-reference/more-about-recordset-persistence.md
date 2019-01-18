---
title: レコードセットの永続化に関する詳細情報
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717609"
---
# <a name="more-about-recordset-persistence"></a>レコードセットの永続化に関する詳細情報

**適用されます**Access 2013、Office 2013。

ADO Recordset オブジェクトは、**Save** メソッドを使用して、ファイルへの [Recordset](save-method-ado.md) オブジェクトの内容の格納をサポートします。 永続的に保存されたファイルには、ローカル ドライブ、ネットワーク サーバー、または web サイトの URL の形式があります。 この永続化されたファイルは、 **Recordset** オブジェクトの [Open](open-method-ado-recordset.md) メソッドまたは [Connection](connection-object-ado.md) オブジェクトの [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッドのいずれかを使用して、後で復元できます。

さらに、[GetString](getstring-method-ado.md) メソッドは、 **Recordset** オブジェクトを、ユーザーが指定した文字で列と行を区切った形式に変換します。

**Recordset** を永続化するには、まず、ファイルに格納できる形式に変換します。 **Recordset** オブジェクトは、Advanced Data TableGram (ADTG) という専用の形式、または公開されている拡張マークアップ言語 (XML) 形式で保存することができます。ADTG の例を以下に示します。XML 永続化の詳細については、「 [レコードを XML 形式で保存する](persisting-records-in-xml-format.md)」を参照してください。

保留中の変更を、永続化されたファイルに保存します。この操作によって、Recordset オブジェクトを返すクエリの発行、Recordset の編集、Recordset および保留中の変更の保存、Recordset の後の復元、保存されている保留中の変更によるデータ ソースの更新などが可能になります。

**Stream** オブジェクトを永続的に保存する方法については、第 10 章の「 [ストリームと永続性](streams-and-persistence.md)」を参照してください。

**Recordset** の永続化の例については、「 [XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。

## <a name="example"></a>使用例

**Recordset の保存**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Recordset.Open を使用して永続化ファイルを開く**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

**Recordset** がアクティブな接続を持たない場合、次のように記述してすべての既定値を受け入れることもできます。

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Connection.Execute を使用して永続化ファイルを開く**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**RDS.DataControl を使用して永続化ファイルを開く**

この場合、 **Server** プロパティは設定されません。

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

