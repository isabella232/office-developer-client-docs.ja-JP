---
title: フィルター適用済みの階層 Recordset を保存する
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 931345aff0cd3d8c9b10c53073e640b3cfdd5de5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889715"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="3b1fe-102">フィルター適用済みの階層 Recordset を保存する</span><span class="sxs-lookup"><span data-stu-id="3b1fe-102">Persisting Filtered and Hierarchical Recordsets</span></span>


<span data-ttu-id="3b1fe-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3b1fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b1fe-p101">[Recordset](filter-property-ado.md) で **Filter** プロパティが有効になっている場合、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合、現在の子 **Recordset** とその子が、親 **Recordset** と共に保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子とそのすべての子は保存されますが、親は保存されません。階層 **Recordset** の詳細については、「 [9 章: データ シェイプ](chapter-9-data-shaping.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b1fe-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="3b1fe-p102">[!メモ] 階層 <STRONG>Recordset</STRONG> (データ シェイプ) を XML 形式で保存する場合、いくつかの制限が適用されます。詳細については、「 <A href="hierarchical-recordsets-in-xml.md">XML の階層 Recordset</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b1fe-p102">Some limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. For more information, see <A href="hierarchical-recordsets-in-xml.md">Hierarchical Recordsets in XML</A>.</span></span></P>


