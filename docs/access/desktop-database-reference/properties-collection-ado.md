---
title: Properties コレクション (ADO)
TOCTitle: Properties Collection (ADO)
ms:assetid: 4d662790-1252-c930-e6f9-edf6a38636af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249245(v=office.15)
ms:contentKeyID: 48544729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231104
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fe2bc84b7d65f49ce742985dab8e1bbe760ecbc5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478065"
---
# <a name="properties-collection-ado"></a><span data-ttu-id="dd6be-102">Properties コレクション (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd6be-102">Properties Collection (ADO)</span></span>


<span data-ttu-id="dd6be-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd6be-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd6be-104">1 つのオブジェクトの特定のインスタンスに対するすべての [Property](property-object-ado.md) オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="dd6be-104">Contains all the [Property](property-object-ado.md) objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd6be-105">備考</span><span class="sxs-lookup"><span data-stu-id="dd6be-105">Remarks</span></span>

<span data-ttu-id="dd6be-p101">一部の ADO オブジェクトには、 **Property** オブジェクトから構成される **Properties** コレクションがあります。各 **Property** オブジェクトは、プロバイダー固有の ADO オブジェクトの特性に対応します。</span><span class="sxs-lookup"><span data-stu-id="dd6be-p101">Some ADO objects have a **Properties** collection made up of **Property** objects. Each **Property** object corresponds to a characteristic of the ADO object specific to the provider.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dd6be-108">[!メモ] <A href="property-object-ado.md">Property</A> オブジェクトの使用方法の詳細については、 <STRONG>Property</STRONG> オブジェクトのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd6be-108">See the <A href="property-object-ado.md">Property</A> object topic for a more detailed explanation of how to use <STRONG>Property</STRONG> objects.</span></span></P>



<span data-ttu-id="dd6be-109">**Recordset** オブジェクトの **動的プロパティ** は、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="dd6be-109">The **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

