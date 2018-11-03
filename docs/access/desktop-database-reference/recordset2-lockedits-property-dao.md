---
title: Recordset2.LockEdits プロパティ (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f93924c579dc32e0841177eeb1068df64e12ab9b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931086"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="23c8a-102">Recordset2.LockEdits プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="23c8a-102">Recordset2.LockEdits property (DAO)</span></span>


<span data-ttu-id="23c8a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="23c8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23c8a-104">編集時に有効になるロック状態の種類を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="23c8a-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c8a-105">構文</span><span class="sxs-lookup"><span data-stu-id="23c8a-105">Syntax</span></span>

<span data-ttu-id="23c8a-106">*式*です。LockEdits</span><span class="sxs-lookup"><span data-stu-id="23c8a-106">*expression* .LockEdits</span></span>

<span data-ttu-id="23c8a-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="23c8a-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c8a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="23c8a-108">Remarks</span></span>

<span data-ttu-id="23c8a-109">次の表は、この設定値または戻り値が表すロック状態の種類です。</span><span class="sxs-lookup"><span data-stu-id="23c8a-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23c8a-110">値</span><span class="sxs-lookup"><span data-stu-id="23c8a-110">Value</span></span></p></th>
<th><p><span data-ttu-id="23c8a-111">説明</span><span class="sxs-lookup"><span data-stu-id="23c8a-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23c8a-112">True</span><span class="sxs-lookup"><span data-stu-id="23c8a-112">True</span></span></p></td>
<td><p><span data-ttu-id="23c8a-p101">既定値です。排他的ロックが有効になります。Edit メソッドを呼び出した直後に、編集中のレコードが含まれているページがロックされます。</span><span class="sxs-lookup"><span data-stu-id="23c8a-p101">Default. Pessimistic locking is in effect. The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23c8a-116">False</span><span class="sxs-lookup"><span data-stu-id="23c8a-116">False</span></span></p></td>
<td><p><span data-ttu-id="23c8a-117">オプティミスティック ロックが有効を編集するためです。</span><span class="sxs-lookup"><span data-stu-id="23c8a-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="23c8a-118">Update メソッドが実行されるまで、レコードを含むページはロックされていません。</span><span class="sxs-lookup"><span data-stu-id="23c8a-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="23c8a-119">**LockEdits** プロパティは、更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="23c8a-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="23c8a-p103">ページがロックされている場合、他のユーザーは同じページのレコードを編集できません。 **LockEdits** プロパティを **True** に設定した場合、 **Edit** メソッドを使用するときに別のユーザーが既にページをロックしていると、エラーが発生します。他のユーザーは、ロックされているページからデータを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="23c8a-p103">If a page is locked, no other user can edit records on the same page. If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method. Other users can read data from locked pages.</span></span>

<span data-ttu-id="23c8a-p104">**LockEdits** プロパティを **False** に設定した場合は、別のユーザーがページをロックしているときに **Update** メソッドを使用すると、エラーが発生します。使用中のレコードに対して別のユーザーが行った変更の内容を表示するには、引数を 0 に設定して **[Move](recordset2-move-method-dao.md)** メソッドを使用します。ただし、このメソッドを実行すると、それまでに行った変更の内容が失われます。</span><span class="sxs-lookup"><span data-stu-id="23c8a-p104">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs. To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="23c8a-p105">Microsoft Access データベース エンジンに接続された ODBC データ ソースを使用する場合は、 **LockEdits** プロパティを常に **False** に設定するか、または共有的ロックを有効にします。Microsoft Access データベース エンジンは、外部のデータベース サーバーで使用されるロック機能に対する制御は行いません。</span><span class="sxs-lookup"><span data-stu-id="23c8a-p105">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking. The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>


> [!NOTE]
> <P><span data-ttu-id="23c8a-127"><STRONG><A href="connection-openrecordset-method-dao.md">何らか</A></STRONG>のメソッドの引数 lockedits を設定して<STRONG>レコード セット</STRONG>を開いたとき、 <STRONG>LockEdits</STRONG>の値を事前設定できます。</span><span class="sxs-lookup"><span data-stu-id="23c8a-127">You can preset the value of <STRONG>LockEdits</STRONG> when you first open the <STRONG>Recordset</STRONG> by setting the lockedits argument of the <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> method.</span></span> <span data-ttu-id="23c8a-128">Lockedits 引数を<STRONG>dbPessimistic</STRONG>に設定に<STRONG>は True</STRONG>、 <STRONG>LockEdits</STRONG>プロパティが設定され、設定 lockedits を他の任意の値には<STRONG>False</STRONG>に<STRONG>LockEdits</STRONG>プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="23c8a-128">Setting the lockedits argument to <STRONG>dbPessimistic</STRONG> will set the <STRONG>LockEdits</STRONG> property to <STRONG>True</STRONG>, and setting lockedits to any other value will set the <STRONG>LockEdits</STRONG> property to <STRONG>False</STRONG>.</span></span></P>



## <a name="example"></a><span data-ttu-id="23c8a-129">例</span><span class="sxs-lookup"><span data-stu-id="23c8a-129">Example</span></span>

<span data-ttu-id="23c8a-p107">この例は、まず **LockEdits** プロパティを **True** に設定して排他的ロックを有効にする方法を示し、次に **LockEdits** プロパティを False に設定して共有的ロックを有効にする方法を示します。また、マルチユーザー データベースの環境でフィールドを変更するために必要なエラー処理の種類を示します。このプロシージャを実行するには、PessimisticLock 関数および OptimisticLock 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="23c8a-p107">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False. It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field. The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
