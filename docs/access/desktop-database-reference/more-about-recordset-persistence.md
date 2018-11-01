---
title: レコードセットの保存の詳細
TOCTitle: More About Recordset Persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: baf1e4976b9669deed0a80f6405127afc88d521e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878293"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="b8056-102">レコードセットの保存の詳細</span><span class="sxs-lookup"><span data-stu-id="b8056-102">More About Recordset Persistence</span></span>


<span data-ttu-id="b8056-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b8056-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8056-104">ADO Recordset オブジェクトは、**Save** メソッドを使用して、ファイルへの [Recordset](save-method-ado.md) オブジェクトの内容の格納をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b8056-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="b8056-105">永続的に保存されたファイルには、ローカル ドライブ、ネットワーク サーバー、または web サイトの URL の形式があります。</span><span class="sxs-lookup"><span data-stu-id="b8056-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="b8056-106">この永続化されたファイルは、 **Recordset** オブジェクトの [Open](open-method-ado-recordset.md) メソッドまたは [Connection](connection-object-ado.md) オブジェクトの [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) メソッドのいずれかを使用して、後で復元できます。</span><span class="sxs-lookup"><span data-stu-id="b8056-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method.</span></span>

<span data-ttu-id="b8056-107">さらに、[GetString](getstring-method-ado.md) メソッドは、 **Recordset** オブジェクトを、ユーザーが指定した文字で列と行を区切った形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="b8056-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="b8056-p102">**Recordset** を永続化するには、まず、ファイルに格納できる形式に変換します。 **Recordset** オブジェクトは、Advanced Data TableGram (ADTG) という専用の形式、または公開されている拡張マークアップ言語 (XML) 形式で保存することができます。ADTG の例を以下に示します。XML 永続化の詳細については、「 [レコードを XML 形式で保存する](persisting-records-in-xml-format.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8056-p102">To persist a **Recordset**, begin by converting it to a form that can be stored in a file. **Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format. ADTG examples are shown below. For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="b8056-p103">保留中の変更を、永続化されたファイルに保存します。この操作によって、Recordset オブジェクトを返すクエリの発行、Recordset の編集、Recordset および保留中の変更の保存、Recordset の後の復元、保存されている保留中の変更によるデータ ソースの更新などが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b8056-p103">Save any pending changes in the persisted file. Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="b8056-114">**Stream** オブジェクトを永続的に保存する方法については、第 10 章の「 [ストリームと永続性](streams-and-persistence.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8056-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="b8056-115">**Recordset** の永続化の例については、「 [XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8056-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="b8056-116">使用例</span><span class="sxs-lookup"><span data-stu-id="b8056-116">Example</span></span>

<span data-ttu-id="b8056-117">**Recordset の保存**</span><span class="sxs-lookup"><span data-stu-id="b8056-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="b8056-118">**Recordset.Open を使用して永続化ファイルを開く**</span><span class="sxs-lookup"><span data-stu-id="b8056-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="b8056-119">**Recordset** がアクティブな接続を持たない場合、次のように記述してすべての既定値を受け入れることもできます。</span><span class="sxs-lookup"><span data-stu-id="b8056-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="b8056-120">**Connection.Execute を使用して永続化ファイルを開く**</span><span class="sxs-lookup"><span data-stu-id="b8056-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="b8056-121">**RDS.DataControl を使用して永続化ファイルを開く**</span><span class="sxs-lookup"><span data-stu-id="b8056-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="b8056-122">この場合、 **Server** プロパティは設定されません。</span><span class="sxs-lookup"><span data-stu-id="b8056-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

