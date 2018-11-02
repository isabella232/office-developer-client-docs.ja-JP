---
title: Recordset2.AddNew メソッド (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67ddd40c6973b323820efbfa67d14c88f0c0b21a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928811"
---
# <a name="recordset2addnew-method-dao"></a>Recordset2.AddNew メソッド (DAO)


**適用されます**Access 2013、Office 2013。
 

更新可能な **Recordset2** オブジェクトの新しいレコードを作成します。

## <a name="syntax"></a>構文

*式*です。AddNew

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**AddNew** メソッドは、レコードセット名で指定された **Recordset2** オブジェクトに新しいレコードを作成および追加するために使用します。このメソッドでは、フィールドが既定値に設定されますが、既定値が指定されていない場合、フィールドは Null (テーブル タイプの **Recordset2** に指定されている既定値) に設定されます。

新しいレコードを追加した後は、 **[Update](recordset2-update-method-dao.md)** メソッドを使用して、変更を保存し、レコードを **Recordset2** に追加します。 **Update** メソッドを使用しない限り、変更はデータベースに反映されません。


> [!NOTE]
> <P>[!メモ] <STRONG>AddNew</STRONG> の実行後、 <STRONG>Update</STRONG> を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。さらに、 <STRONG>Recordset2</STRONG> を終了した場合や、 <STRONG>Recordset2</STRONG> またはその <STRONG><A href="database-object-dao.md">Database</A></STRONG> オブジェクトが宣言されているプロシージャを終了した場合、新しいレコードは警告なしに破棄されます。</P>




> [!NOTE]
> <P>[!メモ] Microsoft Access ワークスペースで <STRONG>AddNew</STRONG> を使用する場合に、データベース エンジンでカレント レコードを保持するために新しいページを作成する必要がある場合は、ページのロック状態は排他的となります。一方、新しいレコードが既存のページに収まる場合は、ページのロック状態は共有的となります。</P>



**Recordset2** の最後のレコードに移動していない場合、他のプロセスによってベース テーブルに追加されたレコードがカレント レコードよりも後ろにある場合は、それらのレコードが含まれる場合があります。しかし、独自の **Recordset2** オブジェクトにレコードを追加する場合は、レコードはその **Recordset2** の他に基になるテーブルにも追加されるため、新しく作成される **Recordset2** オブジェクトにも含まれます。

新しいレコードの位置は、 **Recordset2** の種類によって異なります。

  - ダイナセット タイプの **Recordset2** オブジェクトでは、 **Recordset** を開いたときに有効になっている並べ替え規則や順序規則にかかわらず、 **Recordset** の末尾に挿入されます。

  - [**Index**](recordset2-index-property-dao.md) プロパティが設定されているテーブル タイプの **Recordset2** オブジェクトでは、レコードは並べ替え順序の適切な位置に挿入されて返されます。 **Index** プロパティが設定されていない場合、新しいレコードは **Recordset** の末尾に挿入されて返されます。

**AddNew** を使用する前にカレント レコードであったレコードは、そのままカレント レコードとなります。新しいレコードをカレント レコードにするには、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを **[LastModified](recordset2-lastmodified-property-dao.md)** プロパティの設定で指定されたブックマークに設定します。


> [!NOTE]
> <P>[!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意のインデックスが存在している必要があります。一意のインデックスが存在しない場合、Microsoft Access ワークスペースでは <STRONG>AddNew</STRONG> 、 <STRONG>Delete</STRONG> 、または <STRONG>Edit</STRONG> メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。</P>



## <a name="example"></a>例

この例では、 **AddNew** メソッドを使用して、指定した名前を持つ新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
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
