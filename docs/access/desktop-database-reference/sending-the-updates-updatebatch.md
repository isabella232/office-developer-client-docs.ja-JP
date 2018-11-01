---
title: '更新プログラムを送信する: UpdateBatch'
TOCTitle: 'Sending the Updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 432c54c16984135bb5492854e2a9e9ac1ca94336
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883366"
---
# <a name="sending-the-updates-updatebatch"></a>更新の送信: UpdateBatch


**適用されます**Access 2013、Office 2013。

## <a name="sending-the-updates-updatebatch-method"></a>更新プログラムを送信する: UpdateBatch メソッド

次のコードでは、 **LockType** プロパティを **adLockBatchOptimistic** に、 **CursorLocation** を **adUseClient** に設定することで、 **Recordset** をバッチ モードで開きます。2 つの新規レコードを追加し、既存のレコードのフィールドの値を変更して、元の値を保存した後、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。

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

現在のレコードの編集中、または新規レコードの追加中に **UpdateBatch** メソッドを呼び出すと、変更を一括してプロバイダーに送信する前に、 **Update** メソッドが自動的に呼び出され、現在のレコードの保留中の変更がすべて保存されます。

