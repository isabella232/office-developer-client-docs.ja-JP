---
title: 複数のフィールドの追加
TOCTitle: Adding multiple fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bc9822f2055e7cdfd9a2ef5fe9d2312fc5622ac7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280589"
---
# <a name="adding-multiple-fields"></a><span data-ttu-id="3202f-102">複数のフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="3202f-102">Adding multiple fields</span></span>

<span data-ttu-id="3202f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3202f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3202f-p101">状況によっては、フィールドの配列とそれらのフィールドに対応する値を **AddNew** メソッドに渡す方が、新しいフィールドを 1 つずつ追加して **Value** を何度も設定するよりも効率がよい場合があります。*FieldList* が配列である場合、*Values* も同じ数のメンバーを持つ配列にする必要があり、それ以外のものを指定するとエラーが発生します。また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。フィールドの配列と値の配列を **AddNew** メソッドに渡すコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3202f-p101">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the **AddNew** method, rather than setting **Value** multiple times for each new field. If *FieldList* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs. The order of field names must match the order of field values in each array. The following code passes an array of fields and an array of values to the **AddNew** method.</span></span>

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

