---
title: 更新されたレコードにフィルターを適用する
TOCTitle: Filtering for Updated Records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f95c38da17ded3cc09c4fd8be0ad30342024093
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478699"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="85699-102">更新されたレコードにフィルターを適用する</span><span class="sxs-lookup"><span data-stu-id="85699-102">Filtering for Updated Records</span></span>


<span data-ttu-id="85699-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="85699-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="85699-104">更新されたレコードにフィルターを適用する</span><span class="sxs-lookup"><span data-stu-id="85699-104">Filtering for Updated Records</span></span>

<span data-ttu-id="85699-p101">**UpdateBatch** を呼び出す前に、 **Recordset** の **Filter** プロパティを使用して、 **Recordset** が開かれた後、または **UpdateBatch** が最後に呼び出された後に変更されたレコードだけを表示させることができます。これには、次に示すように、 **Filter** を **adFilterPendingRecords** に設定して、更新されるレコードの数を確認します。</span><span class="sxs-lookup"><span data-stu-id="85699-p101">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**. To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="85699-107">この例では、前に使用した **UpdateBatch** の例を拡張して、 **UpdateBatch** を呼び出す直前に **Recordset** にフィルターを適用しています。これにより、変更されるレコードがユーザーに示され、ユーザーは **CancelBatch** メソッドを使用して更新を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="85699-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

```vb 
 
'BeginFilterAffected 
    objRs1.Filter = adFilterPendingRecords 
    objRs1.MoveFirst 
     
    strMsg = "The following " & objRs1.RecordCount & " values will " & _ 
             "be updated. Do you wish to proceed?" 
    While Not objRs1.EOF 
        strMsg = strMsg & vbCrLf & objRs1(0) & vbTab & objRs1(1) & vbTab & _ 
                 objRs1(2) & vbCrLf 
        objRs1.MoveNext 
    Wend 
     
    blnResp = MsgBox(strMsg, vbYesNo, "Proceed with Update?") 
    If blnResp = True Then 
        objRs1.UpdateBatch 
    Else 
        objRs1.CancelBatch 
    End If 
'EndFilterAffected 
```
