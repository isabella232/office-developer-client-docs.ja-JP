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
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805228"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="296a7-104">[Denoise] セル ([画像のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="296a7-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="296a7-p102">ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。</span><span class="sxs-lookup"><span data-stu-id="296a7-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="296a7-107">備考</span><span class="sxs-lookup"><span data-stu-id="296a7-107">Remarks</span></span>

<span data-ttu-id="296a7-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Denoise] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="296a7-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="296a7-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="296a7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="296a7-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="296a7-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="296a7-111">プログラムから、インデックスによって [Denoise] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="296a7-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="296a7-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="296a7-112">Section index:</span></span>  <br/> |<span data-ttu-id="296a7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="296a7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="296a7-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="296a7-114">Row index:</span></span>  <br/> |<span data-ttu-id="296a7-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="296a7-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="296a7-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="296a7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="296a7-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="296a7-117">**visImageDenoise**</span></span> <br/> |
   

