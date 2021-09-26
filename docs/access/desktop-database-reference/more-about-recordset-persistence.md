---
title: レコードセットの永続化に関する詳細情報
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 97683167d90104d98076f642c5407b6b86a01863
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617959"
---
# <a name="more-about-recordset-persistence"></a>レコードセットの永続化に関する詳細情報

**適用先**: Access 2013、Office 2013

ADO Recordset オブジェクトは、**Save** メソッドを使用して、ファイルへの [Recordset](save-method-ado.md) オブジェクトの内容の格納をサポートします。 永続的に保存されたファイルは、ローカル ドライブ、ネットワーク サーバー、または Web サイト上の URL として存在する可能性があります。 この永続化されたファイルは、 **Recordset** オブジェクトの [Open](open-method-ado-recordset.md) メソッドまたは [Connection](connection-object-ado.md) オブジェクトの [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッドのいずれかを使用して、後で復元できます。

さらに、[GetString](getstring-method-ado.md) メソッドは、 **Recordset** オブジェクトを、ユーザーが指定した文字で列と行を区切った形式に変換します。

**Recordset** を永続化するには、まず、ファイルに格納できる形式に変換します。 **Recordset** オブジェクトは、Advanced Data TableGram (ADTG) という専用の形式、または公開されている拡張マークアップ言語 (XML) 形式で保存することができます。ADTG の例を以下に示します。XML 永続化の詳細については、「 [レコードを XML 形式で保存する](persisting-records-in-xml-format.md)」を参照してください。

Save any pending changes in the persisted file. Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.

**Stream** オブジェクトを永続的に保存する方法については、第 10 章の「 [ストリームと永続性](streams-and-persistence.md)」を参照してください。

**Recordset** の永続化の例については、「[XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。

## <a name="example"></a>例

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

