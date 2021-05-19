---
title: FORMULAEXISTS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033806
localization_priority: Normal
ms.assetid: 3d4f82d3-fcd0-536a-c4e1-94c362cde7c4
description: 参照先のセルに数式が含まれているかどうかを示します。
ms.openlocfilehash: 1f28d429516d4f8b2357f1c2ab589700e38ff40a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420277"
---
# <a name="formulaexists-function"></a><span data-ttu-id="a4352-103">FORMULAEXISTS 関数</span><span class="sxs-lookup"><span data-stu-id="a4352-103">FORMULAEXISTS Function</span></span>

<span data-ttu-id="a4352-104">参照先のセルに数式が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a4352-104">Indicates whether the referenced cell contains a formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a4352-105">構文</span><span class="sxs-lookup"><span data-stu-id="a4352-105">Syntax</span></span>

<span data-ttu-id="a4352-106">FORMULAEXISTS (\*\* *cellref* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a4352-106">FORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a4352-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a4352-107">Parameters</span></span>

|<span data-ttu-id="a4352-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a4352-108">**Name**</span></span>|<span data-ttu-id="a4352-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a4352-109">**Required/Optional**</span></span>|<span data-ttu-id="a4352-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a4352-110">**Data Type**</span></span>|<span data-ttu-id="a4352-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4352-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a4352-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="a4352-112">_cellref_</span></span> <br/> |<span data-ttu-id="a4352-113">必須</span><span class="sxs-lookup"><span data-stu-id="a4352-113">Required</span></span>  <br/> |<span data-ttu-id="a4352-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a4352-114">**String**</span></span> <br/> |<span data-ttu-id="a4352-115">数式があるかどうかを調べるセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="a4352-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4352-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a4352-116">Remarks</span></span>

<span data-ttu-id="a4352-117">セルに数式が含まれている場合、FORMULAEXISTS 関数は 1 を返します。数式を含めない場合は、ゼロ (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="a4352-117">The FORMULAEXISTS function returns 1 if the cell contains a formula; if it does not contain a formula, it returns zero (0).</span></span> 
  

