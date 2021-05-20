---
title: '[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48ab98bd-2966-443c-b3db-befeb271550f
description: 図形に適用されるテーマのコネクタ スキームを整数で指定します。
ms.openlocfilehash: 77d16632db63d187477ba62a1a6f4b9319e156fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437204"
---
# <a name="connectorschemeindex-cell-theme-properties-section"></a><span data-ttu-id="f67bd-103">[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f67bd-103">ConnectorSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="f67bd-104">図形に適用されるテーマのコネクタ スキームを整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="f67bd-104">Determines the connector scheme of a theme that is applied to the shape, as an integer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f67bd-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f67bd-105">Remarks</span></span>

<span data-ttu-id="f67bd-106">別の数式 **、Cell** 要素の **N** 属性の値、または **CellsU** プロパティを使用するプログラムから、名前によって **ConnectorSchemeIndex** セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f67bd-106">To get a reference to the **ConnectorSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f67bd-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="f67bd-107">Cell name:</span></span>  <br/> | <span data-ttu-id="f67bd-108">ConnectorSchemeIndex</span><span class="sxs-lookup"><span data-stu-id="f67bd-108">ConnectorSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="f67bd-109">プログラムから Index によって **ConnectorSchemeIndex** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f67bd-109">To get a reference to the **ConnectorSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f67bd-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f67bd-110">Section index:</span></span>  <br/> |<span data-ttu-id="f67bd-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f67bd-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f67bd-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f67bd-112">Row index:</span></span>  <br/> |<span data-ttu-id="f67bd-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="f67bd-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="f67bd-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f67bd-114">Cell index:</span></span>  <br/> |<span data-ttu-id="f67bd-115">\*\*visConnectorSchemeIndex \*\*</span><span class="sxs-lookup"><span data-stu-id="f67bd-115">\*\*visConnectorSchemeIndex \*\*</span></span> <br/> |
   

