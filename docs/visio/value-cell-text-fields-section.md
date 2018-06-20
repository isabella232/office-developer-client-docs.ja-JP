---
title: '[Value] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: フィールドの関数が格納されます。
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806749"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="242b4-103">[Value] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="242b4-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="242b4-104">フィールドの関数が格納されます。</span><span class="sxs-lookup"><span data-stu-id="242b4-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="242b4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="242b4-105">Remarks</span></span>

<span data-ttu-id="242b4-106">**フィールド**] ダイアログ ボックスを使用してこのセルの値を設定することができます ([**挿入**] タブの [**テキスト**] で、[**フィールド**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="242b4-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="242b4-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [値] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="242b4-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="242b4-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="242b4-108">Cell name:</span></span>  <br/> |<span data-ttu-id="242b4-109">Fields.Value [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="242b4-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="242b4-110">プログラムから、インデックスによって [Value] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="242b4-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="242b4-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="242b4-111">Section index:</span></span>  <br/> |<span data-ttu-id="242b4-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="242b4-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="242b4-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="242b4-113">Row index:</span></span>  <br/> |<span data-ttu-id="242b4-114">**visRowField** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="242b4-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="242b4-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="242b4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="242b4-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="242b4-116">**visFieldCell**</span></span> <br/> |
   

