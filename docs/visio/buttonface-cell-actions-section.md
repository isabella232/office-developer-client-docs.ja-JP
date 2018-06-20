---
title: '[ButtonFace] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804937"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="3f50b-103">[ButtonFace] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="3f50b-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="3f50b-104">ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。</span><span class="sxs-lookup"><span data-stu-id="3f50b-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3f50b-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="3f50b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3f50b-106">注釈</span><span class="sxs-lookup"><span data-stu-id="3f50b-106">Remarks</span></span>

<span data-ttu-id="3f50b-p101">[ButtonFace] セルに含まれる文字列は Microsoft Office のボタン イメージの ID を表します。値ゼロ (0) または空白は、アイコンが表示されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3f50b-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="3f50b-109">ButtonFace] セルに使用できる Id は、 **CommandBarButton**オブジェクトの**FaceID**プロパティで使用される Id と同じです。</span><span class="sxs-lookup"><span data-stu-id="3f50b-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="3f50b-110">これらの Id の詳細については、MSDN の「コマンド バー ボタンのイメージを使用する」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="3f50b-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="3f50b-111">取得する ButtonFace] セルへの参照の名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f50b-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f50b-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="3f50b-112">Cell name:</span></span>  <br/> |<span data-ttu-id="3f50b-113">**アクション**です。</span><span class="sxs-lookup"><span data-stu-id="3f50b-113">**Actions**.</span></span>  <span data-ttu-id="3f50b-114">*名*です。</span><span class="sxs-lookup"><span data-stu-id="3f50b-114">*name*  .</span></span> <span data-ttu-id="3f50b-115">**ButtonFace**で**動作**します。</span><span class="sxs-lookup"><span data-stu-id="3f50b-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="3f50b-116">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="3f50b-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="3f50b-117">プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f50b-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f50b-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f50b-118">Section index:</span></span>  <br/> |<span data-ttu-id="3f50b-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="3f50b-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="3f50b-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f50b-120">Row index:</span></span>  <br/> |<span data-ttu-id="3f50b-121">**visRowAction** +  *i* 、 **i** = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="3f50b-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3f50b-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f50b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3f50b-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="3f50b-123">**visActionButtonFace**</span></span> <br/> |
   

