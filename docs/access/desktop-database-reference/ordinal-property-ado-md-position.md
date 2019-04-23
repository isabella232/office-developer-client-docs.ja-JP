---
title: Ordinal プロパティ (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288191"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="b8380-102">Ordinal プロパティ (ADO MD Position)</span><span class="sxs-lookup"><span data-stu-id="b8380-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="b8380-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8380-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8380-104">軸に沿った位置を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="b8380-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="b8380-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="b8380-105">Return values</span></span>

<span data-ttu-id="b8380-106">長整数型 (**Long**) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="b8380-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8380-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b8380-107">Remarks</span></span>

<span data-ttu-id="b8380-108">[Position](position-object-ado-md.md) オブジェクトの **Ordinal** プロパティは、[Positions](positions-collection-ado-md.md) コレクション内の **Position** のインデックスに対応します。</span><span class="sxs-lookup"><span data-stu-id="b8380-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="b8380-109">**Cellset** オブジェクトの **Item** プロパティでそれぞれの軸に沿って [Position](item-property-ado-md-cellset.md) オブジェクトの [Ordinal](cellset-object-ado-md.md) プロパティを使用することで、セルをすばやく取得できます。</span><span class="sxs-lookup"><span data-stu-id="b8380-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

