---
title: Recordset2 プロパティ (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309243"
---
# <a name="recordset2transactions-property-dao"></a>Recordset2 プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトがトランザクションをサポートしているかどうかを示す値を返します。 値の取得のみ可能なブール型 (**Boolean**) の値です。

## <a name="syntax"></a>構文

*式*。トランザクション

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

Microsoft Access ワークスペースでは、ダイナセット タイプまたはテーブル タイプの **Recordset** オブジェクトでも **Transactions** プロパティを使用できます。 スナップショットおよび前方スクロールタイプの**[Recordset](recordset-object-dao.md)** オブジェクトでは、常に**False**が返されます。

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

