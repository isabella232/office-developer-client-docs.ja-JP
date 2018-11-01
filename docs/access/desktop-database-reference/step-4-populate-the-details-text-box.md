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
# <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="58ef2-102">手順 4: Details テキスト ボックスの値を設定する</span><span class="sxs-lookup"><span data-stu-id="58ef2-102">Step 4: Populate the Details Text Box</span></span>


<span data-ttu-id="58ef2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="58ef2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="58ef2-104">手順 4: Details テキスト ボックスの設定</span><span class="sxs-lookup"><span data-stu-id="58ef2-104">Step 4: Populate the Details Text Box</span></span>

<span data-ttu-id="58ef2-105">**Details テキスト ボックスに値を設定するには**</span><span class="sxs-lookup"><span data-stu-id="58ef2-105">**To populate the Details text box**</span></span>

<span data-ttu-id="58ef2-106">recFields という名前の新しいサブルーチンを作成し、次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="58ef2-106">Create a new subroutine named recFields and insert the following code:</span></span>

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

<span data-ttu-id="58ef2-p101">このコードによって、recFields に渡された単純レコードのフィールドと値が lstDetails に設定されます。リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。このコードで、文字セットが ASCII であるかどうかが判断され、 **Stream** の内容が txtDetails にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="58ef2-p101">This code populates lstDetails with the fields and values of the simple record passed to recFields. If the resource is a text file, a text **Stream** is opened from the resource record. The code determines if the character set is ASCII and copies the **Stream** contents into txtDetails.</span></span>

