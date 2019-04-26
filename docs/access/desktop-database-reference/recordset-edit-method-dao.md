---
title: Recordset.Edit メソッド (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300540"
---
# <a name="recordsetedit-method-dao"></a>Recordset.Edit メソッド (DAO)

**適用先:** Access 2013、Office 2013

現在のレコードを更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトからコピー バッファーにコピーして、後で編集できるようにします。

## <a name="syntax"></a>構文

*expression* .Edit

*expression*: **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Edit** メソッドを使用すると、カレント レコードのフィールドに加えられた変更がコピー バッファーにコピーされます。レコードに必要な変更を加えたら、 **[Update](recordset-update-method-dao.md)** メソッドを使用して変更を保存します。

カレント レコードは、 **Edit** の使用後もカレント レコードのままです。

> [!NOTE]
> [!メモ] レコードの編集後、 **Update** を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。 さらに、レコードセットを閉じた場合や、**Recordset** または親である **[Database](database-object-dao.md)** オブジェクトまたは **[Connection](connection-object-dao.md)** オブジェクトが宣言されているプロシージャを終了した場合は、編集済みのレコードが警告なしに破棄されます。

次の場合は、 **Edit** を使用するとエラーが発生します。

- カレント レコードがない場合。

- **Connection**、 **Database**、または **Recordset** の各オブジェクトが読み取り専用で開かれている場合。

- レコードに更新可能なフィールドがない場合。

- **Database** または **Recordset** が他のユーザーによって排他的に開かれている場合 (Microsoft Access ワークスペース)。

- レコードを含むページが他のユーザーによってロックされている場合 (Microsoft Access ワークスペース)。

Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **[LockEdits](recordset-lockedits-property-dao.md)** プロパティが **True** に設定されている場合 (排他的ロック)、レコードは **Edit** が使用された時点から更新が完了するまでロックされたままになります。 **LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースが更新される直前に、編集前のレコードと比較されます。 **Edit** メソッドを使用した時点からレコードが変更されている場合、 **dbSeeChanges** を指定せずに **OpenRecordset** を使用すると、 **Update** 操作で実行時エラーが発生して更新が失敗します。既定では、Microsoft Access データベース エンジンに接続された ODBC データベースおよびインストール可能な ISAM データベースは、常に共有的ロックを使用します。

> [!NOTE]
> [!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意なインデックスが存在している必要があります。一意なインデックスが存在しない場合、Microsoft Access ワークスペースでは **[AddNew](recordset-addnew-method-dao.md)** 、 **[Delete](fields-delete-method-dao.md)** 、または **Edit** メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。

## <a name="example"></a>例

次の例では、 **Edit** メソッドを使用して、現在のデータを指定された名前に置き換えます。このプロシージャを実行するには、EditName プロシージャが必要です。

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Sub EditName(rstTemp As Recordset, _ 
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
