---
title: '[Denoise] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415805"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="943d6-104">[Denoise] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="943d6-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="943d6-p102">ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。</span><span class="sxs-lookup"><span data-stu-id="943d6-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="943d6-107">注釈</span><span class="sxs-lookup"><span data-stu-id="943d6-107">Remarks</span></span>

<span data-ttu-id="943d6-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Denoise] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="943d6-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="943d6-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="943d6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="943d6-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="943d6-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="943d6-111">プログラムから、インデックスによって [Denoise] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="943d6-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="943d6-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="943d6-112">Section index:</span></span>  <br/> |<span data-ttu-id="943d6-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="943d6-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="943d6-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="943d6-114">Row index:</span></span>  <br/> |<span data-ttu-id="943d6-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="943d6-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="943d6-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="943d6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="943d6-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="943d6-117">**visImageDenoise**</span></span> <br/> |
   

