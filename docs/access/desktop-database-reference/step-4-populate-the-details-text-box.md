---
title: '手順 4: Details テキスト ボックスの値を設定する'
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c00fd9d1a13a68361c5b1a7c3c2aa39736b3c88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867259"
---
# <a name="step-4-populate-the-details-text-box"></a>手順 4: Details テキスト ボックスの値を設定する


**適用されます**Access 2013、Office 2013。

## <a name="step-4-populate-the-details-text-box"></a>手順 4: Details テキスト ボックスの設定

**Details テキスト ボックスに値を設定するには**

recFields という名前の新しいサブルーチンを作成し、次のコードを挿入します。

```vb 
 
Sub recFields(r As Record, l As ListBox, t As TextBox) 
    Dim f As Field 
    Dim s As Stream 
    Set s = New Stream 
    Dim str As String 
     
    For Each f In r.Fields 
        l.AddItem f.Name & ": " & f.Value 
    Next 
    t.Text = "" 
    If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
        s.Open r, adModeRead, adOpenStreamFromRecord 
        str = s.ReadText(1) 
        s.Position = 0 
        If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
            s.Charset = "ascii" 
            s.Type = adTypeText 
        End If 
        t.Text = s.ReadText(adReadAll) 
    End If 
End Sub 
```

このコードによって、recFields に渡された単純レコードのフィールドと値が lstDetails に設定されます。リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。このコードで、文字セットが ASCII であるかどうかが判断され、 **Stream** の内容が txtDetails にコピーされます。

