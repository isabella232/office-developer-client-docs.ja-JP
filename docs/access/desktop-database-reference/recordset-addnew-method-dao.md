---
title: Recordset.AddNew メソッド (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: a09120299915a879de2019de3ba5326cdc8f0c0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606339"
---
# <a name="recordsetaddnew-method-dao"></a>Recordset.AddNew メソッド (DAO)

**適用先**: Access 2013、Office 2013

更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトの新しいレコードを作成します。

## <a name="syntax"></a>構文

*式* .AddNew

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**AddNew** メソッドを使用して、レコードセットによって名付けられた **Recordset** オブジェクトに新しいレコードを作成して追加します。このメソッドによってフィールドは既定値に設定されますが、既定値が指定されていない場合は Null (**Recordset** というテーブル タイプに指定されている既定値) に設定されます。

新しいレコードを編集した後に、 **[Update](recordset-update-method-dao.md)** メソッドを使用して変更内容を保存し、 **Recordset** にレコードを追加します。 **Update** メソッドを使用するまで、データベースは変更されません。

> [!NOTE]
> [!メモ] **AddNew** を実行してから、 **Update** メソッドを使用せずに別のレコードに移動する操作を実行すると、警告なしで変更内容が失われます。また、 **Recordset** を閉じるか、あるいは **Recordset** または **[Database](database-object-dao.md)** オブジェクトを宣言するプロシージャを終了すると、警告なしで新しいレコードが失われます。

> [!NOTE]
> [!メモ] Microsoft Access ワークスペースで **AddNew** を使用し、データベース エンジンがカレント レコードを格納するために新しいページを作成する必要がある場合、ページのロック状態は排他的となります。一方、新しいレコードが既存のページに収まる場合は、ページのロック状態は共有的となります。

**Recordset** の最後のレコードに移動していない場合、他のプロセスでベース テーブルに追加されたレコードがカレント レコード以降に配置された場合は、それらもレコードセットに含まれます。しかし、レコードを自身の **Recordset** に追加する場合は、レコードは **Recordset** に表示され、基になるテーブルに含められるため、すべての新しい **Recordset** オブジェクトで表示されるようになります。

新しいレコードの位置は、 **Recordset** の種類に依存します。

- ダイナセット タイプの **Recordset** オブジェクトでは、 **Recordset** が開かれたときに有効になっていた並べ替えルールにかかわらず、レコードは **Recordset** の最後に追加されます。

- [**Index**](recordset-index-property-dao.md) プロパティが設定されているテーブル タイプの **Recordset** オブジェクトでは、レコードは並べ替え順序に応じた位置に返されます。 **Index** プロパティが設定されていない場合、新しいレコードは **Recordset** の最後に返されます。

**AddNew** を使用する前のカレント レコードは、カレントのままになります。新しいレコードをカレントにするには、 **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを **[LastModified](recordset-lastmodified-property-dao.md)** プロパティの設定によって識別されるブックマークに設定します。

> [!NOTE]
> [!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意なインデックスが存在している必要があります。一意なインデックスが存在しない場合、Microsoft Access ワークスペースでは **AddNew**、 **Delete**、または **Edit** メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。

## <a name="example"></a>例

この例では、 **AddNew** メソッドを使用して、指定した名前を持つ新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
