---
title: Recordset.Transactions プロパティ (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c033ec6f3d80210aaeeb36e9e3eca4b80bfb070d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931317"
---
# <a name="recordsettransactions-property-dao"></a>Recordset.Transactions プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。トランザクション

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

Microsoft Access ワークスペースでは、ダイナセット タイプまたはテーブル タイプの **Recordset** オブジェクトでも **Transactions** プロパティを使用できます。 スナップショット- および前方のみタイプの**[Recordset](recordset-object-dao.md)** オブジェクトは常に**False**を返します。

ダイナセット タイプまたはテーブル タイプの **Recordset** が Microsoft Access データベース エンジン テーブルに基づいている場合、 **Transactions** プロパティは **True** となるため、トランザクションを使用できます。他のデータベース エンジンでは、トランザクションがサポートされていないことがあります。たとえば、Paradox テーブルに基づくダイナセット タイプの **Recordset** オブジェクトでは、トランザクションを使用できません。

**Recordset** オブジェクトの **[Workspace](dbengine-begintrans-method-dao.md)** オブジェクトで [**BeginTrans**](workspace-object-dao.md) メソッドを使用する前に、 **Transactions** プロパティでトランザクションがサポートされているかどうかを確認してください。トランザクションがサポートされていないオブジェクト上で **BeginTrans**、 **CommitTrans**、または **Rollback** の各メソッドを使用しても、何も変化しません。

## <a name="example"></a>例

次の例では、Microsoft Access ワークスペースでの **Transactions** プロパティの機能を示します。

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

