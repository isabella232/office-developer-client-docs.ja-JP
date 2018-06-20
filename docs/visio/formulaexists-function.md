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
ms.openlocfilehash: 9f006cdfed9830734ed2226673ba7566995a58b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805443"
---
# <a name="formulaexists-function"></a><span data-ttu-id="db1b4-103">FORMULAEXISTS 関数</span><span class="sxs-lookup"><span data-stu-id="db1b4-103">FORMULAEXISTS Function</span></span>

<span data-ttu-id="db1b4-104">参照先のセルに数式が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="db1b4-104">Indicates whether the referenced cell contains a formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="db1b4-105">構文</span><span class="sxs-lookup"><span data-stu-id="db1b4-105">Syntax</span></span>

<span data-ttu-id="db1b4-106">FORMULAEXISTS (* * *cellref* * *)</span><span class="sxs-lookup"><span data-stu-id="db1b4-106">FORMULAEXISTS (** *cellref* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="db1b4-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="db1b4-107">Parameters</span></span>

|<span data-ttu-id="db1b4-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="db1b4-108">**Name**</span></span>|<span data-ttu-id="db1b4-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="db1b4-109">**Required/Optional**</span></span>|<span data-ttu-id="db1b4-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="db1b4-110">**Data Type**</span></span>|<span data-ttu-id="db1b4-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="db1b4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="db1b4-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="db1b4-112">_cellref_</span></span> <br/> |<span data-ttu-id="db1b4-113">必須</span><span class="sxs-lookup"><span data-stu-id="db1b4-113">Required</span></span>  <br/> |<span data-ttu-id="db1b4-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="db1b4-114">**String**</span></span> <br/> |<span data-ttu-id="db1b4-115">数式があるかどうかを調べるセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="db1b4-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db1b4-116">注釈</span><span class="sxs-lookup"><span data-stu-id="db1b4-116">Remarks</span></span>

<span data-ttu-id="db1b4-117">FORMULAEXISTS 関数の戻り値を 1 セルに数式が含まれている場合数式を含まない場合は、ゼロ (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="db1b4-117">The FORMULAEXISTS function returns 1 if the cell contains a formula; if it does not contain a formula, it returns zero (0).</span></span> 
  

