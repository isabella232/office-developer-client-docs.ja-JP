---
title: 複数のフィールドを追加する
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9bca4035917f4376ccf69201d79894a0273ceb9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478245"
---
# <a name="adding-multiple-fields"></a><span data-ttu-id="55db4-102">複数のフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="55db4-102">Adding Multiple Fields</span></span>


<span data-ttu-id="55db4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="55db4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="55db4-104">状況によっては、フィールドの配列とそれらのフィールドに対応する値を **AddNew** メソッドに渡す方が、新しいフィールドを 1 つずつ追加して **Value** を何度も設定するよりも効率がよい場合があります。</span><span class="sxs-lookup"><span data-stu-id="55db4-104">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the **AddNew** method, rather than setting **Value** multiple times for each new field.</span></span> <span data-ttu-id="55db4-105">*FieldList*が配列の場合は、*値*配列と同じ数のメンバーにもする必要があります。それ以外の場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="55db4-105">If *FieldList* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="55db4-106">また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="55db4-106">The order of field names must match the order of field values in each array.</span></span> <span data-ttu-id="55db4-107">フィールドの配列と値の配列を **AddNew** メソッドに渡すコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="55db4-107">The following code passes an array of fields and an array of values to the **AddNew** method.</span></span>

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

