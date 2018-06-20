---
title: '[PreviewQuality] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: 図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806084"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="3b251-103">[PreviewQuality] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3b251-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="3b251-104">図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3b251-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="3b251-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3b251-105">**Value**</span></span>|<span data-ttu-id="3b251-106">**プレビューの品質**</span><span class="sxs-lookup"><span data-stu-id="3b251-106">**Preview quality**</span></span>|<span data-ttu-id="3b251-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="3b251-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3b251-108">0</span><span class="sxs-lookup"><span data-stu-id="3b251-108">0</span></span>  <br/> | <span data-ttu-id="3b251-109">ドラフト</span><span class="sxs-lookup"><span data-stu-id="3b251-109">Draft</span></span>  <br/> |<span data-ttu-id="3b251-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="3b251-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="3b251-111">1</span><span class="sxs-lookup"><span data-stu-id="3b251-111">1</span></span>  <br/> | <span data-ttu-id="3b251-112">詳細</span><span class="sxs-lookup"><span data-stu-id="3b251-112">Detailed</span></span>  <br/> |<span data-ttu-id="3b251-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="3b251-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b251-114">備考</span><span class="sxs-lookup"><span data-stu-id="3b251-114">Remarks</span></span>

<span data-ttu-id="3b251-115">[**概要**] タブ、[**プロパティ**] ダイアログ ボックスでこの値を設定することもできます ( **Office**ボタンをクリックして、[**情報**] タブをクリックして、**ドキュメントのプロパティ**] をクリックし、[**詳細プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="3b251-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="3b251-116">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PreviewQuality] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3b251-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b251-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="3b251-117">Cell name:</span></span>  <br/> | <span data-ttu-id="3b251-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="3b251-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="3b251-119">プログラムから、インデックスによって [PreviewQuality] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b251-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b251-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b251-120">Section index:</span></span>  <br/> |<span data-ttu-id="3b251-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b251-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3b251-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b251-122">Row index:</span></span>  <br/> |<span data-ttu-id="3b251-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="3b251-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="3b251-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b251-124">Cell index:</span></span>  <br/> |<span data-ttu-id="3b251-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="3b251-125">**visDocPreviewQuality**</span></span> <br/> |
   

