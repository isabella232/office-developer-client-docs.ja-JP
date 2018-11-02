---
title: TableDef.RefreshLink メソッド (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8b7fda0c095a04d2a3ab7f295497cff05a620ea6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922539"
---
# <a name="tabledefrefreshlink-method-dao"></a><span data-ttu-id="7753f-102">TableDef.RefreshLink メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7753f-102">TableDef.RefreshLink method (DAO)</span></span>

<span data-ttu-id="7753f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7753f-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="7753f-104">リンク テーブルの接続情報を更新します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="7753f-104">Updates the connection information for a linked table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7753f-105">構文</span><span class="sxs-lookup"><span data-stu-id="7753f-105">Syntax</span></span>

<span data-ttu-id="7753f-106">*式*です。RefreshLink</span><span class="sxs-lookup"><span data-stu-id="7753f-106">*expression* .RefreshLink</span></span>

<span data-ttu-id="7753f-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7753f-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7753f-108">解説</span><span class="sxs-lookup"><span data-stu-id="7753f-108">Remarks</span></span>

<span data-ttu-id="7753f-p101">リンク テーブルの接続情報を変更するには、対応する [TableDef](connection-connect-property-dao.md) オブジェクトの \*\*\*\*Connect\*\*\*\* プロパティをリセットした上で、 **RefreshLink** メソッドを使用して情報を更新します。 **RefreshLink** メソッドを使用しても、リンク テーブルのプロパティ、および **[Relation](relation-object-dao.md)** オブジェクトは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7753f-p101">To change the connection information for a linked table, reset the **[Connect](connection-connect-property-dao.md)** property of the corresponding **TableDef** object and then use the **RefreshLink** method to update the information. Using **RefreshLink** method doesn't change the linked table's properties and **[Relation](relation-object-dao.md)** objects.</span></span>

<span data-ttu-id="7753f-111">リンク テーブルを表す **TableDef** オブジェクトに関連付けられたすべてのコレクションにこの接続情報を反映するには、各コレクションで **[Refresh](tabledefs-refresh-method-dao.md)** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7753f-111">For this connection information to exist in all collections associated with the **TableDef** object that represents the linked table, you must use the **[Refresh](tabledefs-refresh-method-dao.md)** method on each collection.</span></span>

## <a name="example"></a><span data-ttu-id="7753f-112">例</span><span class="sxs-lookup"><span data-stu-id="7753f-112">Example</span></span>

<span data-ttu-id="7753f-p102">この例では、 **RefreshLink** メソッドを使用して、リンク テーブルの接続が、あるデータ ソースから別のデータ ソースに変更された後に、リンク テーブルのデータを更新します。このプロシージャを実行するには、RefreshLinkOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="7753f-p102">This example uses the **RefreshLink** method to refresh the data in a linked table after its connection has been changed from one data source to another. The RefreshLinkOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

