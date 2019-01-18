---
title: Recordset2.AddNew メソッド (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 49a69b5e8603e72faaba480ea9069d3668bd6de1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699346"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="e402d-102">Recordset2.AddNew メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="e402d-102">Recordset2.AddNew method (DAO)</span></span>

<span data-ttu-id="e402d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e402d-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="e402d-104">更新可能な **Recordset2** オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="e402d-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e402d-105">構文</span><span class="sxs-lookup"><span data-stu-id="e402d-105">Syntax</span></span>

<span data-ttu-id="e402d-106">*式*です。AddNew</span><span class="sxs-lookup"><span data-stu-id="e402d-106">*expression* .AddNew</span></span>

<span data-ttu-id="e402d-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="e402d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e402d-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e402d-108">Remarks</span></span>

<span data-ttu-id="e402d-p101">**AddNew** メソッドは、レコードセット名で指定された **Recordset2** オブジェクトに新しいレコードを作成および追加するために使用します。このメソッドでは、フィールドが既定値に設定されますが、既定値が指定されていない場合、フィールドは Null (テーブル タイプの **Recordset2** に指定されている既定値) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e402d-p101">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="e402d-p102">新しいレコードを追加した後は、 **[Update](recordset2-update-method-dao.md)** メソッドを使用して、変更を保存し、レコードを **Recordset2** に追加します。 **Update** メソッドを使用しない限り、変更はデータベースに反映されません。</span><span class="sxs-lookup"><span data-stu-id="e402d-p102">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**. No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="e402d-p103">[!メモ] **AddNew** の実行後、 **Update** を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。さらに、 **Recordset2** を終了した場合や、 **Recordset2** またはその **[Database](database-object-dao.md)** オブジェクトが宣言されているプロシージャを終了した場合、新しいレコードは警告なしに破棄されます。</span><span class="sxs-lookup"><span data-stu-id="e402d-p103">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning. In addition, if you close the **Recordset2** or end the procedure that declares the **Recordset2** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="e402d-p104">[!メモ] Microsoft Access ワークスペースで **AddNew** を使用する場合に、データベース エンジンでカレント レコードを保持するために新しいページを作成する必要がある場合は、ページのロック状態は排他的となります。一方、新しいレコードが既存のページに収まる場合は、ページのロック状態は共有的となります。</span><span class="sxs-lookup"><span data-stu-id="e402d-p104">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="e402d-p105">**Recordset2** の最後のレコードに移動していない場合、他のプロセスによってベース テーブルに追加されたレコードがカレント レコードよりも後ろにある場合は、それらのレコードが含まれる場合があります。しかし、独自の **Recordset2** オブジェクトにレコードを追加する場合は、レコードはその **Recordset2** の他に基になるテーブルにも追加されるため、新しく作成される **Recordset2** オブジェクトにも含まれます。</span><span class="sxs-lookup"><span data-stu-id="e402d-p105">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="e402d-119">新しいレコードの位置は、 **Recordset2** の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e402d-119">The position of the new record depends on the type of **Recordset2**:</span></span>

- <span data-ttu-id="e402d-120">ダイナセット タイプの **Recordset2** オブジェクトでは、 **Recordset** を開いたときに有効になっている並べ替え規則や順序規則にかかわらず、 **Recordset** の末尾に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="e402d-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="e402d-p106">[**Index**](recordset2-index-property-dao.md) プロパティが設定されているテーブル タイプの **Recordset2** オブジェクトでは、レコードは並べ替え順序の適切な位置に挿入されて返されます。 **Index** プロパティが設定されていない場合、新しいレコードは **Recordset** の末尾に挿入されて返されます。</span><span class="sxs-lookup"><span data-stu-id="e402d-p106">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="e402d-p107">**AddNew** を使用する前にカレント レコードであったレコードは、そのままカレント レコードとなります。新しいレコードをカレント レコードにするには、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを **[LastModified](recordset2-lastmodified-property-dao.md)** プロパティの設定で指定されたブックマークに設定します。</span><span class="sxs-lookup"><span data-stu-id="e402d-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="e402d-p108">[!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意のインデックスが存在している必要があります。一意のインデックスが存在しない場合、Microsoft Access ワークスペースでは **AddNew** 、 **Delete** 、または **Edit** メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e402d-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="e402d-127">例</span><span class="sxs-lookup"><span data-stu-id="e402d-127">Example</span></span>

<span data-ttu-id="e402d-p109">この例では、 **AddNew** メソッドを使用して、指定した名前を持つ新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="e402d-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
