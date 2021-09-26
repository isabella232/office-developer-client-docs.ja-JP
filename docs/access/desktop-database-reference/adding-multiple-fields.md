---
title: 複数のフィールドの追加
TOCTitle: Adding multiple fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 41833d744ef94e50d011014401db6a48ef68a416
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590178"
---
# <a name="adding-multiple-fields"></a>複数のフィールドの追加

**適用先**: Access 2013、Office 2013

状況によっては、フィールドの配列とそれらのフィールドに対応する値を **AddNew** メソッドに渡す方が、新しいフィールドを 1 つずつ追加して **Value** を何度も設定するよりも効率がよい場合があります。*FieldList* が配列である場合、*Values* も同じ数のメンバーを持つ配列にする必要があり、それ以外のものを指定するとエラーが発生します。また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。フィールドの配列と値の配列を **AddNew** メソッドに渡すコードを次に示します。

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

