---
title: Properties コレクション (ADO)
TOCTitle: Properties collection (ADO)
ms:assetid: 4d662790-1252-c930-e6f9-edf6a38636af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249245(v=office.15)
ms:contentKeyID: 48544729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231104
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d64f879f6a65226656bd510703e8b5b0ac8f71a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706486"
---
# <a name="properties-collection-ado"></a><span data-ttu-id="cbbb8-102">Properties コレクション (ADO)</span><span class="sxs-lookup"><span data-stu-id="cbbb8-102">Properties collection (ADO)</span></span>

<span data-ttu-id="cbbb8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cbbb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbbb8-104">1 つのオブジェクトの特定のインスタンスに対するすべての [Property](property-object-ado.md) オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="cbbb8-104">Contains all the [Property](property-object-ado.md) objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbbb8-105">備考</span><span class="sxs-lookup"><span data-stu-id="cbbb8-105">Remarks</span></span>

<span data-ttu-id="cbbb8-p101">一部の ADO オブジェクトには、 **Property** オブジェクトから構成される **Properties** コレクションがあります。各 **Property** オブジェクトは、プロバイダー固有の ADO オブジェクトの特性に対応します。</span><span class="sxs-lookup"><span data-stu-id="cbbb8-p101">Some ADO objects have a **Properties** collection made up of **Property** objects. Each **Property** object corresponds to a characteristic of the ADO object specific to the provider.</span></span>

> [!NOTE]
> <span data-ttu-id="cbbb8-108">[!メモ] [Property](property-object-ado.md) オブジェクトの使用方法の詳細については、 **Property** オブジェクトのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbbb8-108">See the [Property](property-object-ado.md) object topic for a more detailed explanation of how to use **Property** objects.</span></span>

<span data-ttu-id="cbbb8-109">**Recordset** オブジェクトの **動的プロパティ** は、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="cbbb8-109">The **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

