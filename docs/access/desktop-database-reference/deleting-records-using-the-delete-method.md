---
title: Delete メソッドを使用してレコードを削除します。
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8f9097f791596f45f574749d98919b61f67cb4f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944495"
---
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="c9fb4-102">Delete メソッドを使用してレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-102">Deleting records using the Delete method</span></span>


<span data-ttu-id="c9fb4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9fb4-p101">**Delete** メソッドを使用すると、 **Recordset** オブジェクト内の現在のレコード、またはレコードのグループが削除されるよう設定されます。 **Recordset** オブジェクトでレコードの削除が認められていない場合は、エラーが発生します。イミディエイト更新モードを使用している場合、削除操作はデータベース内で直ちに実行されます。データベースの整合性違反などによってレコードの削除が正常に実行できない場合、レコードは **Update** が呼び出された後も編集モードのまま変化しません。このため、 [Close](cancelupdate-method-ado.md)、[Move](close-method-ado.md)、[NextRecordset](move-method-ado.md) などを使用して現在のレコードから移動する前に、 [CancelUpdate](nextrecordset-method-ado.md) を使用して更新を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p101">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion. If the **Recordset** object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="c9fb4-p102">バッチ更新モードを使用している場合、レコードはキャッシュから削除されるよう設定され、実際の削除は **UpdateBatch** メソッドを呼び出したときに実行されます (削除されたレコードを表示するには、 **Delete** を呼び出した後に **Filter** プロパティを **adFilterAffectedRecords** に設定します)。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p102">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method. (To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="c9fb4-p103">削除されたレコードからフィールド値を取得しようとすると、エラーが生成されます。現在のレコードが削除された後も、他のレコードに移動するまで、削除されたレコードが現在のレコードとなります。削除されたレコードから移動すると、それ以降そのレコードにはアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p103">Attempting to retrieve field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="c9fb4-p104">削除操作をトランザクション内に入れ子にしている場合は、 **RollbackTrans** メソッドを使用して削除されたレコードを元に戻すことができます。バッチ更新モードを使用している場合は、 **CancelBatch** メソッドを使用して、1 つまたは複数の保留中の削除操作を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p104">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="c9fb4-p105">基になるデータとの競合 (レコードが他のユーザーによって既に削除されている場合など) によって、レコードの削除操作が失敗した場合、プロバイダーは **Errors** コレクションに警告を返しますが、プログラムの実行は停止されません。実行時エラーが発生するのは、すべての要求されたレコードに競合がある場合のみです。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p105">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="c9fb4-118">動的プロパティである **Unique Table** が設定されており、 **Recordset** が複数のテーブルに対して JOIN 操作を実行した結果である場合、 **Delete** メソッドを使用すると、 **Unique Table** プロパティで指定されたテーブルの行のみが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="c9fb4-p106">**Delete** メソッドは、 **Delete** 操作の対象となるレコードを指定できるオプションの引数を受け取ります。この引数に指定できる値は、次の ADO **AffectEnum** 列挙定数のうちどちらかのみです。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p106">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation. The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="c9fb4-121">**adAffectCurrent**現在のレコードのみに影響します。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-121">**adAffectCurrent**Affects only the current record.</span></span>

  - <span data-ttu-id="c9fb4-122">**adAffectGroup**現在の**Filter**プロパティの設定を満たすレコードのみに影響します。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-122">**adAffectGroup**Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="c9fb4-123">このオプションを使用するには、 **Filter** プロパティが、 **FilterGroupEnum** 値、または **Bookmarks** の配列に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="c9fb4-p108">次のコードでは、 **Delete** メソッドを呼び出すときに **adAffectGroup** を指定する例を示します。この例では、いくつかのレコードをサンプルの **Recordset** に追加し、データベースを更新します。次に、フィルター列挙定数である **adFilterAffectedRecords** 使用して **Recordset** をフィルター処理し、新しく追加されたレコードのみ **Recordset** 内に表示されるようにします。最後に、 **Delete** メソッドを呼び出し、現在の **Filter** プロパティの設定を満たすすべてのレコード (新しいレコード) を削除するよう指定します。</span><span class="sxs-lookup"><span data-stu-id="c9fb4-p108">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method. This example adds some records to the sample **Recordset** and updates the database. Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**. Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

