---
title: DBEngine.Idle メソッド (DAO)
TOCTitle: Idle Method
description: Idle メソッド
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/14/2021
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0c476e335bc14392ccac304108b9df3056fd7548
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581463"
---
# <a name="dbengineidle-method-dao"></a>DBEngine.Idle メソッド (DAO)

**適用先:** Access 2013、Office 2013

データの処理を中断し、Microsoft Access データベース エンジンでメモリの最適化やページのタイムアウトなどのタスクを完了できるようにします (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .Idle(***Action***)

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

|**名前**|**必須かどうか**|**データ型**|**説明**|
|:----------|:----------|:----------|:----------|
|*Action*|オプション|**Variant**|実行するアクションを指定します。|

## <a name="remarks"></a>注釈

**Idle** メソッドを使用すると、データ処理の負荷が高いために最新の状態でない可能性のあるバックグラウンド タスクを Microsoft Access データベース エンジンで実行できるようになります。たとえば、マルチユーザー/マルチタスキングの環境で、 **[Recordset](recordset-object-dao.md)** 内のすべてのレコードを最新の状態に保つためのバックグラウンド処理に必要な時間が十分でない場合に、データが最新の状態でないことがあります。

通常は、他のアクション (マウスの移動を含む) が発生していない場合のみ、読み取りロックが解除され、ローカルにあるダイナセット タイプの **Recordset** オブジェクトのデータが更新されます。 **Idle** メソッドを定期的に使用すると、不要な読み取りロックが解除され、バックグラウンド処理のタスクの遅れを取り戻すことができます。

任意指定の引数 **dbRefreshCache** を指定すると、データベースの最新のデータのみを使用してメモリが更新されます。

シングルユーザー環境の場合は、1 つのアプリケーションの複数のインスタンスを実行していない限り、このメソッドを使用する必要はありません。 **Idle** メソッドを使用すると、メモリのロックが解除され、データが強制的にディスクに書き込まれるため、マルチユーザー環境の場合はこのメソッドを使用することによりパフォーマンスが向上することがあります。


> [!NOTE]
> [!メモ] 操作をトランザクションの一部にすることにより、読み取りロックを解除することもできます。

## <a name="example"></a>例

次の使用例では、 **Idle** メソッドを使用して、出力プロシージャがデータベースの最新のデータにアクセスできるようにします。このプロシージャを実行するには、IdleOutput プロシージャが必要です。

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```
