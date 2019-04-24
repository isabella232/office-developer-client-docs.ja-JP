---
title: Recordset2 メソッド (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309437"
---
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="502c1-102">Recordset2 メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="502c1-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="502c1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="502c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="502c1-104">更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトからカレント レコードをコピー バッファーにコピーし、編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="502c1-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="502c1-105">構文</span><span class="sxs-lookup"><span data-stu-id="502c1-105">Syntax</span></span>

<span data-ttu-id="502c1-106">*式*。修正</span><span class="sxs-lookup"><span data-stu-id="502c1-106">*expression* .Edit</span></span>

<span data-ttu-id="502c1-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="502c1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="502c1-108">注釈</span><span class="sxs-lookup"><span data-stu-id="502c1-108">Remarks</span></span>

<span data-ttu-id="502c1-p101">**Edit** メソッドを使用すると、カレント レコードのフィールドに加えられた変更がコピー バッファーにコピーされます。レコードに必要な変更を加えたら、 **[Update](recordset2-update-method-dao.md)** メソッドを使用して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="502c1-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="502c1-111">カレント レコードは、 **Edit** の使用後もカレント レコードのままです。</span><span class="sxs-lookup"><span data-stu-id="502c1-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="502c1-112">[!メモ] レコードの編集後、 **Update** を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。</span><span class="sxs-lookup"><span data-stu-id="502c1-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="502c1-113">また、recordset を閉じるか、または**recordset**または親**[データベース](database-object-dao.md)** または**[Connection](connection-object-dao.md)** オブジェクトを宣言するプロシージャを終了すると、編集したレコードは警告なしに破棄されます。</span><span class="sxs-lookup"><span data-stu-id="502c1-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="502c1-114">次の場合は、 **Edit** を使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="502c1-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="502c1-115">カレント レコードがない場合。</span><span class="sxs-lookup"><span data-stu-id="502c1-115">There is no current record.</span></span>

- <span data-ttu-id="502c1-116">**Connection**、 **Database**、または **Recordset** の各オブジェクトが読み取り専用で開かれている場合。</span><span class="sxs-lookup"><span data-stu-id="502c1-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="502c1-117">レコードに更新可能なフィールドがない場合。</span><span class="sxs-lookup"><span data-stu-id="502c1-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="502c1-118">**Database** または **Recordset** が他のユーザーによって排他的に開かれている場合 (Microsoft Access ワークスペース)。</span><span class="sxs-lookup"><span data-stu-id="502c1-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="502c1-119">レコードを含むページが他のユーザーによってロックされている場合 (Microsoft Access ワークスペース)。</span><span class="sxs-lookup"><span data-stu-id="502c1-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="502c1-p103">Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **[LockEdits](recordset2-lockedits-property-dao.md)** プロパティが **True** に設定されている場合 (排他的ロック)、レコードは **Edit** が使用された時点から更新が完了するまでロックされたままになります。 **LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースが更新される直前に、編集前のレコードと比較されます。 **Edit** メソッドを使用した時点からレコードが変更されている場合、 **dbSeeChanges** を指定せずに **OpenRecordset** を使用すると、 **Update** 操作で実行時エラーが発生して更新が失敗します。既定では、Microsoft Access データベース エンジンに接続された ODBC データベースおよびインストール可能な ISAM データベースは、常に共有的ロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="502c1-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="502c1-p104">[!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意なインデックスが存在している必要があります。一意なインデックスが存在しない場合、Microsoft Access ワークスペースでは **[AddNew](recordset2-addnew-method-dao.md)** 、 **[Delete](fields-delete-method-dao.md)** 、または **Edit** メソッドを呼び出したときに "アクセスが拒否されました。" のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="502c1-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="502c1-126">例</span><span class="sxs-lookup"><span data-stu-id="502c1-126">Example</span></span>

<span data-ttu-id="502c1-p105">次の例では、 **Edit** メソッドを使用して、現在のデータを指定された名前に置き換えます。このプロシージャを実行するには、EditName プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="502c1-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

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
