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
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805776"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="08514-103">[LockTextEdit] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="08514-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="08514-104">図形のテキストをロックして、編集できないようにします。</span><span class="sxs-lookup"><span data-stu-id="08514-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="08514-105">**値**</span><span class="sxs-lookup"><span data-stu-id="08514-105">**Value**</span></span>|<span data-ttu-id="08514-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="08514-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08514-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="08514-107">TRUE</span></span>  <br/> |<span data-ttu-id="08514-108">テキストを編集できません。</span><span class="sxs-lookup"><span data-stu-id="08514-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="08514-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="08514-109">FALSE</span></span>  <br/> | <span data-ttu-id="08514-110">テキストを編集できます。</span><span class="sxs-lookup"><span data-stu-id="08514-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08514-111">注釈</span><span class="sxs-lookup"><span data-stu-id="08514-111">Remarks</span></span>

<span data-ttu-id="08514-112">テキストの書式設定**テキスト**] ダイアログ ボックスでスタイルを適用することができますもする ([**ホーム**] タブで、[**フォント**の矢印] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="08514-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="08514-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockTextEdit] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="08514-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08514-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="08514-114">Cell name:</span></span>  <br/> | <span data-ttu-id="08514-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="08514-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="08514-116">プログラムから、インデックスによって [LockTextEdit] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="08514-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08514-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="08514-117">Section index:</span></span>  <br/> |<span data-ttu-id="08514-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08514-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="08514-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="08514-119">Row index:</span></span>  <br/> |<span data-ttu-id="08514-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="08514-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="08514-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="08514-121">Cell index:</span></span>  <br/> |<span data-ttu-id="08514-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="08514-122">**visLockTextEdit**</span></span> <br/> |
   

