---
title: Recordset2.AddNew メソッド (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e8123fc67d8b41b892f92b19605a26384af68b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477746"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="7ffb2-102">Recordset2.AddNew メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ffb2-102">Recordset2.AddNew Method (DAO)</span></span>


<span data-ttu-id="7ffb2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ffb2-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="7ffb2-104">更新可能な **Recordset2** オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffb2-105">構文</span><span class="sxs-lookup"><span data-stu-id="7ffb2-105">Syntax</span></span>

<span data-ttu-id="7ffb2-106">*式*です。AddNew</span><span class="sxs-lookup"><span data-stu-id="7ffb2-106">*expression* .AddNew</span></span>

<span data-ttu-id="7ffb2-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffb2-108">注釈</span><span class="sxs-lookup"><span data-stu-id="7ffb2-108">Remarks</span></span>

<span data-ttu-id="7ffb2-p101">**AddNew** メソッドは、レコードセット名で指定された **Recordset2** オブジェクトに新しいレコードを作成および追加するために使用します。このメソッドでは、フィールドが既定値に設定されますが、既定値が指定されていない場合、フィールドは Null (テーブル タイプの **Recordset2** に指定されている既定値) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p101">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="7ffb2-p102">新しいレコードを追加した後は、 **[Update](recordset2-update-method-dao.md)** メソッドを使用して、変更を保存し、レコードを **Recordset2** に追加します。 **Update** メソッドを使用しない限り、変更はデータベースに反映されません。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p102">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7ffb2-p103">[!メモ] <STRONG>AddNew</STRONG> の実行後、 <STRONG>Update</STRONG> を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。さらに、 <STRONG>Recordset2</STRONG> を終了した場合や、 <STRONG>Recordset2</STRONG> またはその <STRONG><A href="database-object-dao.md">Database</A></STRONG> オブジェクトが宣言されているプロシージャを終了した場合、新しいレコードは警告なしに破棄されます。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset2</STRONG> or end the procedure that declares the <STRONG>Recordset2</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="7ffb2-p104">[!メモ] Microsoft Access ワークスペースで <STRONG>AddNew</STRONG> を使用する場合に、データベース エンジンでカレント レコードを保持するために新しいページを作成する必要がある場合は、ページのロック状態は排他的となります。一方、新しいレコードが既存のページに収まる場合は、ページのロック状態は共有的となります。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="7ffb2-p105">**Recordset2** の最後のレコードに移動していない場合、他のプロセスによってベース テーブルに追加されたレコードがカレント レコードよりも後ろにある場合は、それらのレコードが含まれる場合があります。しかし、独自の **Recordset2** オブジェクトにレコードを追加する場合は、レコードはその **Recordset2** の他に基になるテーブルにも追加されるため、新しく作成される **Recordset2** オブジェクトにも含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p105">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="7ffb2-119">新しいレコードの位置は、 **Recordset2** の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-119">The position of the new record depends on the type of **Recordset2**:</span></span>

  - <span data-ttu-id="7ffb2-120">ダイナセット タイプの **Recordset2** オブジェクトでは、 **Recordset** を開いたときに有効になっている並べ替え規則や順序規則にかかわらず、 **Recordset** の末尾に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="7ffb2-p106">[**Index**](recordset2-index-property-dao.md) プロパティが設定されているテーブル タイプの **Recordset2** オブジェクトでは、レコードは並べ替え順序の適切な位置に挿入されて返されます。 **Index** プロパティが設定されていない場合、新しいレコードは **Recordset** の末尾に挿入されて返されます。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p106">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="7ffb2-p107">**AddNew** を使用する前にカレント レコードであったレコードは、そのままカレント レコードとなります。新しいレコードをカレント レコードにするには、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを **[LastModified](recordset2-lastmodified-property-dao.md)** プロパティの設定で指定されたブックマークに設定します。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7ffb2-p108">[!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意のインデックスが存在している必要があります。一意のインデックスが存在しない場合、Microsoft Access ワークスペースでは <STRONG>AddNew</STRONG> 、 <STRONG>Delete</STRONG> 、または <STRONG>Edit</STRONG> メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="7ffb2-127">例</span><span class="sxs-lookup"><span data-stu-id="7ffb2-127">Example</span></span>

<span data-ttu-id="7ffb2-p109">この例では、 **AddNew** メソッドを使用して、指定した名前を持つ新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="7ffb2-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
