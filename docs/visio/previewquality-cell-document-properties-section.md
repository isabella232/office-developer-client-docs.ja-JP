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
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356036"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="c4869-103">[PreviewQuality] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="c4869-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="c4869-104">図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4869-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="c4869-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c4869-105">**Value**</span></span>|<span data-ttu-id="c4869-106">**プレビューの品質**</span><span class="sxs-lookup"><span data-stu-id="c4869-106">**Preview quality**</span></span>|<span data-ttu-id="c4869-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="c4869-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c4869-108">.0</span><span class="sxs-lookup"><span data-stu-id="c4869-108">0</span></span>  <br/> | <span data-ttu-id="c4869-109">Draft</span><span class="sxs-lookup"><span data-stu-id="c4869-109">Draft</span></span>  <br/> |<span data-ttu-id="c4869-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="c4869-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="c4869-111">1-d</span><span class="sxs-lookup"><span data-stu-id="c4869-111">1</span></span>  <br/> | <span data-ttu-id="c4869-112">詳細</span><span class="sxs-lookup"><span data-stu-id="c4869-112">Detailed</span></span>  <br/> |<span data-ttu-id="c4869-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="c4869-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4869-114">解説</span><span class="sxs-lookup"><span data-stu-id="c4869-114">Remarks</span></span>

<span data-ttu-id="c4869-115">この値は、[**プロパティ**] ダイアログボックスの [**概要**] タブで設定することもできます ( **Office**ボタンをクリックし、[**情報**] タブをクリックし、[**ドキュメントのプロパティ**] をクリックし、[**詳細プロパティ**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c4869-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="c4869-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PreviewQuality] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c4869-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4869-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="c4869-117">Cell name:</span></span>  <br/> | <span data-ttu-id="c4869-118">[previewquality]</span><span class="sxs-lookup"><span data-stu-id="c4869-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="c4869-119">プログラムから、インデックスによって [PreviewQuality] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4869-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4869-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c4869-120">Section index:</span></span>  <br/> |<span data-ttu-id="c4869-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4869-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c4869-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c4869-122">Row index:</span></span>  <br/> |<span data-ttu-id="c4869-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="c4869-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="c4869-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c4869-124">Cell index:</span></span>  <br/> |<span data-ttu-id="c4869-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="c4869-125">**visDocPreviewQuality**</span></span> <br/> |
   

