---
title: 更新済みのレコードのフィルター処理
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7d65ae6765cc5bf3ddf5b6fefcdf6b2b5e295fba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602620"
---
# <a name="filtering-for-updated-records"></a>更新済みのレコードのフィルター処理

**適用先**: Access 2013、Office 2013

## <a name="filtering-for-updated-records"></a>更新されたレコードにフィルターを適用する

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

