---
title: Recordset2.Edit メソッド (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2742b6558c555673937666ea7d27cae1a54fdf73
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707746"
---
# <a name="recordset2edit-method-dao"></a>Recordset2.Edit メソッド (DAO)

**適用されます**Access 2013、Office 2013。

更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトからカレント レコードをコピー バッファーにコピーし、編集できるようにします。

## <a name="syntax"></a>構文

*式*です。編集

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Edit** メソッドを使用すると、カレント レコードのフィールドに加えられた変更がコピー バッファーにコピーされます。レコードに必要な変更を加えたら、 **[Update](recordset2-update-method-dao.md)** メソッドを使用して変更を保存します。

カレント レコードは、 **Edit** の使用後もカレント レコードのままです。

> [!NOTE]
> [!メモ] レコードの編集後、 **Update** を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。 さらに、レコード セットを閉じるか、**レコード セット**または親の**[データベース](database-object-dao.md)** または**[接続](connection-object-dao.md)** オブジェクトを宣言するプロシージャを終了した場合は、警告なし、編集されたレコードが破棄されます。

次の場合は、 **Edit** を使用するとエラーが発生します。

- カレント レコードがない場合

- **Connection** 、 **Database** 、または **Recordset** の各オブジェクトが読み取り専用で開かれている場合。

- 更新可能なフィールドがレコードにない場合

- **Database** または **Recordset** が他のユーザーによって排他的に開かれている場合 (Microsoft Access ワークスペース)。

- レコードを格納しているページが別のユーザーによってロックされている場合 (Microsoft Access ワークスペース)

Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **[LockEdits](recordset2-lockedits-property-dao.md)** プロパティが **True** に設定されている場合 (排他的ロック)、レコードは **Edit** が使用された時点から更新が完了するまでロックされたままになります。 **LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースが更新される直前に、編集前のレコードと比較されます。 **Edit** メソッドを使用した時点からレコードが変更されている場合、 **dbSeeChanges** を指定せずに **OpenRecordset** を使用すると、 **Update** 操作で実行時エラーが発生して更新が失敗します。既定では、Microsoft Access データベース エンジンに接続された ODBC データベースおよびインストール可能な ISAM データベースは、常に共有的ロックを使用します。

> [!NOTE]
> [!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意のインデックスが存在している必要があります。一意のインデックスが存在しない場合、Microsoft Access ワークスペースでは **[AddNew](recordset2-addnew-method-dao.md)** 、 **[Delete](fields-delete-method-dao.md)** 、または **Edit** メソッドを呼び出したときに「アクセスが拒否されました」のエラーが発生します。

## <a name="example"></a>例

この例では、 **Edit** メソッドを使用して、現在のデータを指定された名前に置き換えます。このプロシージャを実行するには、EditName プロシージャが必要です。

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
