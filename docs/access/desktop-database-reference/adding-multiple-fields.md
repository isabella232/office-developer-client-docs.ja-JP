---
title: 複数のフィールドを追加します。
TOCTitle: Adding multiple fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ea9b4999ae107c6b6ca88ca7cf75888163a5b05
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944110"
---
# <a name="adding-multiple-fields"></a>複数のフィールドを追加します。

**適用されます**Access 2013、Office 2013。

状況によっては、フィールドの配列とそれらのフィールドに対応する値を **AddNew** メソッドに渡す方が、新しいフィールドを 1 つずつ追加して **Value** を何度も設定するよりも効率がよい場合があります。 *FieldList*が配列の場合は、*値*配列と同じ数のメンバーにもする必要があります。それ以外の場合、エラーが発生します。 また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。 フィールドの配列と値の配列を **AddNew** メソッドに渡すコードを次に示します。

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

