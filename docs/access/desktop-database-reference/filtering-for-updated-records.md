---
title: 更新されたレコードのフィルタ リング
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3bf6619b9b375642bc9f279aea92cb20df3b859
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947813"
---
# <a name="filtering-for-updated-records"></a>更新されたレコードのフィルタ リング

**適用されます**Access 2013、Office 2013。

## <a name="filtering-for-updated-records"></a>更新済みのレコードのフィルター処理

**UpdateBatch** を呼び出す前に、 **Recordset** の **Filter** プロパティを使用して、 **Recordset** が開かれた後、または **UpdateBatch** が最後に呼び出された後に変更されたレコードだけを表示させることができます。これには、次に示すように、 **Filter** を **adFilterPendingRecords** に設定して、更新されるレコードの数を確認します。

この例では、前に使用した **UpdateBatch** の例を拡張して、 **UpdateBatch** を呼び出す直前に **Recordset** にフィルターを適用しています。これにより、変更されるレコードがユーザーに示され、ユーザーは **CancelBatch** メソッドを使用して更新を取り消すことができます。

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

