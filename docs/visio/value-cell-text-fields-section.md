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
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320203"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="8f09c-103">[Value] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="8f09c-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="8f09c-104">フィールドの関数が格納されます。</span><span class="sxs-lookup"><span data-stu-id="8f09c-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f09c-105">解説</span><span class="sxs-lookup"><span data-stu-id="8f09c-105">Remarks</span></span>

<span data-ttu-id="8f09c-106">このセルの値は、[**フィールド**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**テキスト**] グループで、[**フィールド**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="8f09c-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="8f09c-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Value] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f09c-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f09c-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="8f09c-108">Cell name:</span></span>  <br/> |<span data-ttu-id="8f09c-109">フィールドの値 [ *i* ]。 *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="8f09c-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8f09c-110">プログラムから、インデックスによって [Value] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8f09c-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f09c-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8f09c-111">Section index:</span></span>  <br/> |<span data-ttu-id="8f09c-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="8f09c-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="8f09c-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8f09c-113">Row index:</span></span>  <br/> |<span data-ttu-id="8f09c-114">**visRowField** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="8f09c-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8f09c-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8f09c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8f09c-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="8f09c-116">**visFieldCell**</span></span> <br/> |
   

