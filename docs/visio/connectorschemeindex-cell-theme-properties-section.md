---
title: '[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48ab98bd-2966-443c-b3db-befeb271550f
description: 図形に適用されるテーマのコネクタスキームを整数で指定します。
ms.openlocfilehash: 77d16632db63d187477ba62a1a6f4b9319e156fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437204"
---
# <a name="connectorschemeindex-cell-theme-properties-section"></a><span data-ttu-id="f0b88-103">[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f0b88-103">ConnectorSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="f0b88-104">図形に適用されるテーマのコネクタスキームを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="f0b88-104">Determines the connector scheme of a theme that is applied to the shape, as an integer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f0b88-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f0b88-105">Remarks</span></span>

<span data-ttu-id="f0b88-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[connectorschemeindex]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f0b88-106">To get a reference to the **ConnectorSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0b88-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="f0b88-107">Cell name:</span></span>  <br/> | <span data-ttu-id="f0b88-108">[connectorschemeindex]</span><span class="sxs-lookup"><span data-stu-id="f0b88-108">ConnectorSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="f0b88-109">プログラムから、インデックスによって [ **[connectorschemeindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0b88-109">To get a reference to the **ConnectorSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0b88-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0b88-110">Section index:</span></span>  <br/> |<span data-ttu-id="f0b88-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0b88-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f0b88-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0b88-112">Row index:</span></span>  <br/> |<span data-ttu-id="f0b88-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="f0b88-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="f0b88-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0b88-114">Cell index:</span></span>  <br/> |<span data-ttu-id="f0b88-115">\* \* visConnectorSchemeIndex \* \*</span><span class="sxs-lookup"><span data-stu-id="f0b88-115">\*\*visConnectorSchemeIndex \*\*</span></span> <br/> |
   

