---
title: LOCALFORMULAEXISTS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: 参照先のセルにローカル数式が含まれているかどうかを示します。
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433291"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="8cb30-103">LOCALFORMULAEXISTS 関数</span><span class="sxs-lookup"><span data-stu-id="8cb30-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="8cb30-104">参照先のセルにローカル数式が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8cb30-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8cb30-105">構文</span><span class="sxs-lookup"><span data-stu-id="8cb30-105">Syntax</span></span>

<span data-ttu-id="8cb30-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8cb30-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8cb30-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8cb30-107">Parameters</span></span>

|<span data-ttu-id="8cb30-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="8cb30-108">**Name**</span></span>|<span data-ttu-id="8cb30-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="8cb30-109">**Required/Optional**</span></span>|<span data-ttu-id="8cb30-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="8cb30-110">**Data Type**</span></span>|<span data-ttu-id="8cb30-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="8cb30-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8cb30-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="8cb30-112">_cellref_</span></span> <br/> |<span data-ttu-id="8cb30-113">必須</span><span class="sxs-lookup"><span data-stu-id="8cb30-113">Required</span></span>  <br/> |<span data-ttu-id="8cb30-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8cb30-114">**String**</span></span> <br/> | <span data-ttu-id="8cb30-115">数式があるかどうかを調べるセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="8cb30-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8cb30-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="8cb30-116">Return value</span></span>

<span data-ttu-id="8cb30-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="8cb30-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8cb30-118">注釈</span><span class="sxs-lookup"><span data-stu-id="8cb30-118">Remarks</span></span>

<span data-ttu-id="8cb30-119">LOCALFORMULAEXISTS 関数は、セルがローカルの数式を含む場合は 1 を返し、数式がないか、数式が継承されている場合は 0 (ゼロ) を返します。</span><span class="sxs-lookup"><span data-stu-id="8cb30-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

