---
title: '更新プログラムを送信する: UpdateBatch'
TOCTitle: 'Sending the Updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df52f5bf2dbada1176a76cda3b77dcbc9966b313
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476949"
---
# <a name="sending-the-updates-updatebatch"></a><span data-ttu-id="a5f29-102">更新プログラムを送信する: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="a5f29-102">Sending the Updates: UpdateBatch</span></span>


<span data-ttu-id="a5f29-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5f29-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="sending-the-updates-updatebatch-method"></a><span data-ttu-id="a5f29-104">更新プログラムを送信する: UpdateBatch メソッド</span><span class="sxs-lookup"><span data-stu-id="a5f29-104">Sending the Updates: UpdateBatch Method</span></span>

<span data-ttu-id="a5f29-p101">次のコードでは、 **LockType** プロパティを **adLockBatchOptimistic** に、 **CursorLocation** を **adUseClient** に設定することで、 **Recordset** をバッチ モードで開きます。2 つの新規レコードを追加し、既存のレコードのフィールドの値を変更して、元の値を保存した後、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="a5f29-p101">The following code opens a **Recordset** in batch mode by setting the **LockType** property to **adLockBatchOptimistic** and the **CursorLocation** to **adUseClient**. It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls **UpdateBatch** to send the changes back to the data source.</span></span>

```vb 
 
'BeginBatchUpdate 
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers" 
                  
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
     
    ' Change value of Phone field for first record in Recordset, saving value 
    ' for later restoration. 
    intId = objRs1("ShipperId") 
    strPhone = objRs1("Phone") 
     
    objRs1("Phone") = "(111) 555-1111" 
     
    'Add two new records 
    For i = 0 To 1 
        objRs1.AddNew 
        objRs1(1) = "New Shipper #" & CStr((i + 1)) 
        objRs1(2) = "(nnn) 555-" & i & i & i & i 
    Next i 
     
    ' Send the updates 
    objRs1.UpdateBatch 
'EndBatchUpdate 
```

<span data-ttu-id="a5f29-107">現在のレコードの編集中、または新規レコードの追加中に **UpdateBatch** メソッドを呼び出すと、変更を一括してプロバイダーに送信する前に、 **Update** メソッドが自動的に呼び出され、現在のレコードの保留中の変更がすべて保存されます。</span><span class="sxs-lookup"><span data-stu-id="a5f29-107">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

