---
title: '[LockTextEdit] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: 図形のテキストをロックして、編集できないようにします。
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348315"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="985ec-103">[LockTextEdit] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="985ec-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="985ec-104">図形のテキストをロックして、編集できないようにします。</span><span class="sxs-lookup"><span data-stu-id="985ec-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="985ec-105">**値**</span><span class="sxs-lookup"><span data-stu-id="985ec-105">**Value**</span></span>|<span data-ttu-id="985ec-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="985ec-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="985ec-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="985ec-107">TRUE</span></span>  <br/> |<span data-ttu-id="985ec-108">テキストを編集できません。</span><span class="sxs-lookup"><span data-stu-id="985ec-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="985ec-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="985ec-109">FALSE</span></span>  <br/> | <span data-ttu-id="985ec-110">テキストを編集できます。</span><span class="sxs-lookup"><span data-stu-id="985ec-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="985ec-111">解説</span><span class="sxs-lookup"><span data-stu-id="985ec-111">Remarks</span></span>

<span data-ttu-id="985ec-112">ロックされている場合でも、[**テキスト**] ダイアログ ボックスでスタイルを適用することにより、テキストの書式設定を行うことはできます (このダイアログ ボックスを開くには、[**ホーム**] タブで、[**フォント**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="985ec-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="985ec-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockTextEdit] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="985ec-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="985ec-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="985ec-114">Cell name:</span></span>  <br/> | <span data-ttu-id="985ec-115">[locktextedit]</span><span class="sxs-lookup"><span data-stu-id="985ec-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="985ec-116">プログラムから、インデックスによって [LockTextEdit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="985ec-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="985ec-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="985ec-117">Section index:</span></span>  <br/> |<span data-ttu-id="985ec-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="985ec-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="985ec-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="985ec-119">Row index:</span></span>  <br/> |<span data-ttu-id="985ec-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="985ec-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="985ec-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="985ec-121">Cell index:</span></span>  <br/> |<span data-ttu-id="985ec-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="985ec-122">**visLockTextEdit**</span></span> <br/> |
   

