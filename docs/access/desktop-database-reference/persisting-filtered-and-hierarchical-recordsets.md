---
title: フィルター適用、階層レコード セットを永続化します。
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13255bcd5cd40745a767b8aff9f49449b0127294
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946119"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="69d71-102">フィルター適用、階層レコード セットを永続化します。</span><span class="sxs-lookup"><span data-stu-id="69d71-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="69d71-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="69d71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69d71-p101">[Recordset](filter-property-ado.md) で **Filter** プロパティが有効になっている場合、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合、現在の子 **Recordset** とその子が、親 **Recordset** と共に保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子とそのすべての子は保存されますが、親は保存されません。階層 **Recordset** の詳細については、「 [9 章: データ シェイプ](chapter-9-data-shaping.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69d71-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="69d71-p102">[!メモ] 階層 **Recordset** (データ シェイプ) を XML 形式で保存する場合、いくつかの制限が適用されます。詳細については、「 [XML の階層 Recordset](hierarchical-recordsets-in-xml.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69d71-p102">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format. For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


