---
title: NOT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Logicalexpression が FALSE の場合は、TRUE (1) を返します。 それ以外の場合、FALSE (0) を返します。
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805927"
---
# <a name="not-function"></a><span data-ttu-id="fa822-104">NOT 関数</span><span class="sxs-lookup"><span data-stu-id="fa822-104">NOT Function</span></span>

<span data-ttu-id="fa822-105">_Logicalexpression_が FALSE の場合は、TRUE (1) を返します。</span><span class="sxs-lookup"><span data-stu-id="fa822-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="fa822-106">それ以外の場合、FALSE (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="fa822-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fa822-107">構文</span><span class="sxs-lookup"><span data-stu-id="fa822-107">Syntax</span></span>

<span data-ttu-id="fa822-108">されません (* * *logicalexpression* * *)</span><span class="sxs-lookup"><span data-stu-id="fa822-108">NOT(** *logicalexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fa822-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa822-109">Parameters</span></span>

|<span data-ttu-id="fa822-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="fa822-110">**Name**</span></span>|<span data-ttu-id="fa822-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fa822-111">**Required/Optional**</span></span>|<span data-ttu-id="fa822-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fa822-112">**Data Type**</span></span>|<span data-ttu-id="fa822-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="fa822-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fa822-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="fa822-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="fa822-115">必須</span><span class="sxs-lookup"><span data-stu-id="fa822-115">Required</span></span>  <br/> |<span data-ttu-id="fa822-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="fa822-116">**String**</span></span> <br/> |<span data-ttu-id="fa822-117">評価する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="fa822-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fa822-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa822-118">Return value</span></span>

<span data-ttu-id="fa822-119">ブール型 (Boolean)。</span><span class="sxs-lookup"><span data-stu-id="fa822-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="fa822-120">例</span><span class="sxs-lookup"><span data-stu-id="fa822-120">Example</span></span>

<span data-ttu-id="fa822-121">しない (高さ\>0.75 で)</span><span class="sxs-lookup"><span data-stu-id="fa822-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="fa822-p103">Height が 0.75 インチ以下の場合は、1 を返します。Height が 0.75 インチより大きい場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="fa822-p103">Returns 1 if Height is less than or equal to 0.75 inches. Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

