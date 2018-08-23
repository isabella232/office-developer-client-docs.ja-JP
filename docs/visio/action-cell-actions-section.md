---
title: '[Action] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804750"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="34b19-103">[Action] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="34b19-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="34b19-104">ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。</span><span class="sxs-lookup"><span data-stu-id="34b19-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="34b19-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="34b19-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="34b19-106">備考</span><span class="sxs-lookup"><span data-stu-id="34b19-106">Remarks</span></span>

<span data-ttu-id="34b19-107">[Action] セルは、アクションが発生したときにのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="34b19-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="34b19-108">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Action] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="34b19-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34b19-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="34b19-109">Cell name:</span></span>  <br/> | <span data-ttu-id="34b19-110">アクションです。</span><span class="sxs-lookup"><span data-stu-id="34b19-110">Actions.</span></span>  <span data-ttu-id="34b19-111">*名*です。アクション、アクション。</span><span class="sxs-lookup"><span data-stu-id="34b19-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="34b19-112">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="34b19-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="34b19-113">プログラムから、インデックスによって [Action] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="34b19-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34b19-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="34b19-114">Section index:</span></span>  <br/> |<span data-ttu-id="34b19-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="34b19-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="34b19-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="34b19-116">Row index:</span></span>  <br/> |<span data-ttu-id="34b19-117">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="34b19-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="34b19-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="34b19-118">Cell index:</span></span>  <br/> |<span data-ttu-id="34b19-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="34b19-119">**visActionAction**</span></span> <br/> |
   

