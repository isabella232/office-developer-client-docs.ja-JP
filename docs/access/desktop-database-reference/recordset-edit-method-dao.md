---
title: Recordset.Edit メソッド (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76868140d9f6f1b16a35219864d054ed1f742e84
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996483"
---
# <a name="recordsetedit-method-dao"></a><span data-ttu-id="48e5a-102">Recordset.Edit メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="48e5a-102">Recordset.Edit method (DAO)</span></span>

<span data-ttu-id="48e5a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="48e5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48e5a-104">更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトからカレント レコードをコピー バッファーにコピーし、編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="48e5a-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e5a-105">構文</span><span class="sxs-lookup"><span data-stu-id="48e5a-105">Syntax</span></span>

<span data-ttu-id="48e5a-106">*式*です。編集</span><span class="sxs-lookup"><span data-stu-id="48e5a-106">*expression* .Edit</span></span>

<span data-ttu-id="48e5a-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="48e5a-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="48e5a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="48e5a-108">Remarks</span></span>

<span data-ttu-id="48e5a-p101">**Edit** メソッドを使用すると、カレント レコードのフィールドに加えられた変更がコピー バッファーにコピーされます。レコードに必要な変更を加えたら、 **[Update](recordset-update-method-dao.md)** メソッドを使用して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="48e5a-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="48e5a-111">カレント レコードは、 **Edit** の使用後もカレント レコードのままです。</span><span class="sxs-lookup"><span data-stu-id="48e5a-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="48e5a-112">[!メモ] レコードの編集後、 **Update** を使用せずに他のレコードへ移動する操作を行った場合、変更は警告なしに取り消されます。</span><span class="sxs-lookup"><span data-stu-id="48e5a-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="48e5a-113">さらに、レコード セットを閉じるか、**レコード セット**または親の**[データベース](database-object-dao.md)** または**[接続](connection-object-dao.md)** オブジェクトを宣言するプロシージャを終了した場合は、警告なし、編集されたレコードが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="48e5a-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="48e5a-114">次の場合は、 **Edit** を使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="48e5a-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="48e5a-115">カレント レコードがない場合</span><span class="sxs-lookup"><span data-stu-id="48e5a-115">There is no current record.</span></span>

- <span data-ttu-id="48e5a-116">**Connection** 、 **Database** 、または **Recordset** の各オブジェクトが読み取り専用で開かれている場合。</span><span class="sxs-lookup"><span data-stu-id="48e5a-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="48e5a-117">更新可能なフィールドがレコードにない場合</span><span class="sxs-lookup"><span data-stu-id="48e5a-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="48e5a-118">**Database** または **Recordset** が他のユーザーによって排他的に開かれている場合 (Microsoft Access ワークスペース)。</span><span class="sxs-lookup"><span data-stu-id="48e5a-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="48e5a-119">レコードを格納しているページが別のユーザーによってロックされている場合 (Microsoft Access ワークスペース)</span><span class="sxs-lookup"><span data-stu-id="48e5a-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="48e5a-p103">Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **[LockEdits](recordset-lockedits-property-dao.md)** プロパティが **True** に設定されている場合 (排他的ロック)、レコードは **Edit** が使用された時点から更新が完了するまでロックされたままになります。 **LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースが更新される直前に、編集前のレコードと比較されます。 **Edit** メソッドを使用した時点からレコードが変更されている場合、 **dbSeeChanges** を指定せずに **OpenRecordset** を使用すると、 **Update** 操作で実行時エラーが発生して更新が失敗します。既定では、Microsoft Access データベース エンジンに接続された ODBC データベースおよびインストール可能な ISAM データベースは、常に共有的ロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="48e5a-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="48e5a-p104">[!メモ] レコードを追加、編集、削除するには、基になるデータ ソースのレコードに一意のインデックスが存在している必要があります。一意のインデックスが存在しない場合、Microsoft Access ワークスペースでは **[AddNew](recordset-addnew-method-dao.md)** 、 **[Delete](fields-delete-method-dao.md)** 、または **Edit** メソッドを呼び出したときに「アクセスが拒否されました」のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="48e5a-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="48e5a-126">例</span><span class="sxs-lookup"><span data-stu-id="48e5a-126">Example</span></span>

<span data-ttu-id="48e5a-p105">この例では、 **Edit** メソッドを使用して、現在のデータを指定された名前に置き換えます。このプロシージャを実行するには、EditName プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="48e5a-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

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
