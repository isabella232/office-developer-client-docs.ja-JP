---
title: '[Layer Membership] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2080
localization_priority: Normal
ms.assetid: 7fb1d8a1-8892-f489-2f58-0008b5b750f5
description: 図形が割り当てられる各レイヤーを一覧表示する行を格納します。
ms.openlocfilehash: 5f522e31916ad276e15ac23e5149407dd67eb9cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805682"
---
# <a name="layer-membership-section"></a><span data-ttu-id="93c6b-103">[レイヤー メンバーシップ] セクション</span><span class="sxs-lookup"><span data-stu-id="93c6b-103">Layer Membership Section</span></span>

<span data-ttu-id="93c6b-104">図形が割り当てられる各レイヤーを一覧表示する行を格納します。</span><span class="sxs-lookup"><span data-stu-id="93c6b-104">Contains one row that lists each layer to which the shape is assigned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93c6b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="93c6b-105">Remarks</span></span>

<span data-ttu-id="93c6b-p101">レイヤーの割り当ては、ページ上にあるレイヤーの一覧のインデックスとして表示されます。レイヤーのインデックスは、[**レイヤー プロパティ**] ダイアログ ボックスに表示されるレイヤーの順番に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。ダイアログ ボックスの最初の名前は、layer 0 です。2 番目は layer 1 で、以降続きます。</span><span class="sxs-lookup"><span data-stu-id="93c6b-p101">The layer assignment is shown as an index to the list of layers on the page. The layer index corresponds to the order of the layers in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**). The first name in the dialog box is layer 0, the second is layer 1, and so forth.</span></span>
  
<span data-ttu-id="93c6b-109">図形が複数のレイヤーに割り当てられている場合、各レイヤーのインデックスは、[Layer Membership] セルに、セミコロンで区切られて表示されます。</span><span class="sxs-lookup"><span data-stu-id="93c6b-109">If a shape is assigned to more than one layer, each layer index appears in the Layer Membership cell separated by a semicolon.</span></span>
  
<span data-ttu-id="93c6b-110">数式で [Layer Membership] セルの値を参照するには、 **LayerMember**の名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="93c6b-110">To refer to the value of the Layer Membership cell in a formula, use the name **LayerMember**.</span></span>
  

