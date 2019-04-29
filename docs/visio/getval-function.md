---
title: GETVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: セルの値を取得します。セルの値が変更されても、数式は再計算されません。
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416889"
---
# <a name="getval-function"></a><span data-ttu-id="20c38-103">GETVAL 関数</span><span class="sxs-lookup"><span data-stu-id="20c38-103">GETVAL Function</span></span>

<span data-ttu-id="20c38-104">セルの値を取得します。セルの値が変更されても、数式は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="20c38-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="20c38-105">構文</span><span class="sxs-lookup"><span data-stu-id="20c38-105">Syntax</span></span>

<span data-ttu-id="20c38-106">getval (\* \* *cellname* \* \*)</span><span class="sxs-lookup"><span data-stu-id="20c38-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20c38-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20c38-107">Parameters</span></span>

|<span data-ttu-id="20c38-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="20c38-108">**Name**</span></span>|<span data-ttu-id="20c38-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="20c38-109">**Required/Optional**</span></span>|<span data-ttu-id="20c38-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="20c38-110">**Data Type**</span></span>|<span data-ttu-id="20c38-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="20c38-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20c38-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="20c38-112">_cellname_</span></span> <br/> |<span data-ttu-id="20c38-113">必須</span><span class="sxs-lookup"><span data-stu-id="20c38-113">Required</span></span>  <br/> |<span data-ttu-id="20c38-114">**String**</span><span class="sxs-lookup"><span data-stu-id="20c38-114">**String**</span></span> <br/> |<span data-ttu-id="20c38-115">値を取得するセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="20c38-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="20c38-116">例</span><span class="sxs-lookup"><span data-stu-id="20c38-116">Example</span></span>

<span data-ttu-id="20c38-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="20c38-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="20c38-118">[PinX]、[PinY]、[Width] の各セルの値の合計を返します。</span><span class="sxs-lookup"><span data-stu-id="20c38-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

