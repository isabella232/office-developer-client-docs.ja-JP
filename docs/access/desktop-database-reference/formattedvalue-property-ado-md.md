---
title: FormattedValue プロパティ (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d750944cd42feb95b09f53382c54329ea0c32e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292315"
---
# <a name="formattedvalue-property-ado-md"></a><span data-ttu-id="c9cc8-102">FormattedValue プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c9cc8-102">FormattedValue property (ADO MD)</span></span>


<span data-ttu-id="c9cc8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9cc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9cc8-104">セル値の書式付き表示を示します。</span><span class="sxs-lookup"><span data-stu-id="c9cc8-104">Indicates the formatted display of a cell value.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9cc8-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9cc8-105">Return values</span></span>

<span data-ttu-id="c9cc8-106">文字列型 (**String**) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="c9cc8-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9cc8-107">注釈</span><span class="sxs-lookup"><span data-stu-id="c9cc8-107">Remarks</span></span>

<span data-ttu-id="c9cc8-p101">**FormattedValue** プロパティを使用すると、[Cell](cell-object-ado-md.md) オブジェクトの [Value](value-property-ado-md.md) プロパティの書式付き表示の値を取得できます。たとえば、セルの値が 1056.87 で、この値がドルの額を表している場合、**FormattedValue** プロパティは $1,056.87 になります。</span><span class="sxs-lookup"><span data-stu-id="c9cc8-p101">Use the **FormattedValue** property to obtain the formatted display value of the [Value](value-property-ado-md.md) property of a [Cell](cell-object-ado-md.md) object. For example, if the value of a cell was 1056.87, and this value represented a dollar amount, **FormattedValue** would be $1,056.87.</span></span>

