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
ms.openlocfilehash: b9a9a5624697779bb7231626b7440d8db9c40244
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996819"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="ec590-102">Recordset.AddNew メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ec590-102">Recordset.AddNew method (DAO)</span></span>

<span data-ttu-id="ec590-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ec590-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec590-104">更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="ec590-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec590-105">構文</span><span class="sxs-lookup"><span data-stu-id="ec590-105">Syntax</span></span>

<span data-ttu-id="ec590-106">*式*です。AddNew</span><span class="sxs-lookup"><span data-stu-id="ec590-106">*expression* .AddNew</span></span>

<span data-ttu-id="ec590-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ec590-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec590-108">備考</span><span class="sxs-lookup"><span data-stu-id="ec590-108">Remarks</span></span>

<span data-ttu-id="ec590-p101">**AddNew** メソッドを使用して、レコードセットによって名付けられた **Recordset** オブジェクトに新しいレコードを作成して追加します。このメソッドによってフィールドは既定値に設定されますが、既定値が指定されていない場合は Null (**Recordset** というテーブル タイプに指定されている既定値) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ec590-p101">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="ec590-p102">新しいレコードを編集した後に、 **[Update](recordset-update-method-dao.md)** メソッドを使用して変更内容を保存し、 **Recordset** にレコードを追加します。 **Update** メソッドを使用するまで、データベースは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ec590-p102">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**. No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="ec590-p103">[!メモ] **AddNew** を実行してから、 **Update** メソッドを使用せずに別のレコードに移動する操作を実行すると、警告なしで変更内容が失われます。また、 **Recordset** を閉じるか、あるいは **Recordset** または **[Database](database-object-dao.md)** オブジェクトを宣言するプロシージャを終了すると、警告なしで新しいレコードが失われます。</span><span class="sxs-lookup"><span data-stu-id="ec590-p103">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning. In addition, if you close the **Recordset** or end the procedure that declares the **Recordset** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="ec590-p104">[!メモ] Microsoft Access ワークスペースで **AddNew** を使用し、データベース エンジンがカレント レコードを格納するために新しいページを作成する必要がある場合、ページのロック状態は排他的となります。一方、新しいレコードが既存のページに収まる場合は、ページのロック状態は共有的となります。</span><span class="sxs-lookup"><span data-stu-id="ec590-p104">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="ec590-p105">**Recordset** の最後のレコードに移動していない場合、他のプロセスでベース テーブルに追加されたレコードがカレント レコード以降に配置された場合は、それらもレコードセットに含まれます。しかし、レコードを自身の **Recordset** に追加する場合は、レコードは **Recordset** に表示され、基になるテーブルに含められるため、すべての新しい **Recordset** オブジェクトで表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="ec590-p105">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="ec590-119">新しいレコードの位置は、 **Recordset** の種類に依存します。</span><span class="sxs-lookup"><span data-stu-id="ec590-119">The position of the new record depends on the type of **Recordset**:</span></span>

- <span data-ttu-id="ec590-120">ダイナセット タイプの **Recordset** オブジェクトでは、 **Recordset** が開かれたときに有効になっていた並べ替えルールにかかわらず、レコードは **Recordset** の最後に追加されます。</span><span class="sxs-lookup"><span data-stu-id="ec590-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="ec590-p106">[**Index**](recordset-index-property-dao.md) プロパティが設定されているテーブル タイプの **Recordset** オブジェクトでは、レコードは並べ替え順序に応じた位置に返されます。 **Index** プロパティが設定されていない場合、新しいレコードは **Recordset** の最後に返されます。</span><span class="sxs-lookup"><span data-stu-id="ec590-p106">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="ec590-p107">**AddNew** を使用する前のカレント レコードは、カレントのままになります。新しいレコードをカレントにするには、 **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを **[LastModified](recordset-lastmodified-property-dao.md)** プロパティの設定によって識別されるブックマークに設定します。</span><span class="sxs-lookup"><span data-stu-id="ec590-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="ec590-p108">[!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意のインデックスが存在している必要があります。一意のインデックスが存在しない場合、Microsoft Access ワークスペースでは **AddNew** 、 **Delete** 、または **Edit** メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ec590-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="ec590-127">例</span><span class="sxs-lookup"><span data-stu-id="ec590-127">Example</span></span>

<span data-ttu-id="ec590-p109">この例では、 **AddNew** メソッドを使用して、指定した名前を持つ新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="ec590-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
