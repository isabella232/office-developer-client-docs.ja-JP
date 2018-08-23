---
title: AND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: TRUE をすべての論理式を指定する場合は、TRUE (1) を返します。 FALSE または 0 の論理式のいずれかの場合は、AND 関数は FALSE (0) を返します。
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804786"
---
# <a name="and-function"></a><span data-ttu-id="f4b6e-104">AND 関数</span><span class="sxs-lookup"><span data-stu-id="f4b6e-104">AND Function</span></span>

<span data-ttu-id="f4b6e-105">TRUE をすべての論理式を指定する場合は、TRUE (1) を返します。</span><span class="sxs-lookup"><span data-stu-id="f4b6e-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="f4b6e-106">FALSE または 0 の論理式のいずれかの場合は、AND 関数は FALSE (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="f4b6e-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f4b6e-107">構文</span><span class="sxs-lookup"><span data-stu-id="f4b6e-107">Syntax</span></span>

<span data-ttu-id="f4b6e-108">(* **論理 expression1* * *、* **論理式 2* * *,...、* **論理 expressionN* * *)</span><span class="sxs-lookup"><span data-stu-id="f4b6e-108">AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f4b6e-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4b6e-109">Parameters</span></span>

|<span data-ttu-id="f4b6e-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="f4b6e-110">**Name**</span></span>|<span data-ttu-id="f4b6e-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f4b6e-111">**Required/Optional**</span></span>|<span data-ttu-id="f4b6e-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f4b6e-112">**Data Type**</span></span>|<span data-ttu-id="f4b6e-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="f4b6e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f4b6e-114">_論理式_</span><span class="sxs-lookup"><span data-stu-id="f4b6e-114">_logical expression_</span></span> <br/> |<span data-ttu-id="f4b6e-115">必須</span><span class="sxs-lookup"><span data-stu-id="f4b6e-115">Required</span></span>  <br/> |<span data-ttu-id="f4b6e-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f4b6e-116">**String**</span></span> <br/> | <span data-ttu-id="f4b6e-p103">定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。ゼロ以外の値に評価される式はすべて TRUE であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="f4b6e-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="f4b6e-119">例</span><span class="sxs-lookup"><span data-stu-id="f4b6e-119">Example</span></span>

<span data-ttu-id="f4b6e-120">(高さ\>1 の場合、[pinx] \> 1)</span><span class="sxs-lookup"><span data-stu-id="f4b6e-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="f4b6e-p104">両方の式が TRUE の場合、TRUE を返します。いずれかの式が FALSE の場合、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f4b6e-p104">Returns TRUE if both expressions are TRUE. Returns FALSE if either expression is FALSE.</span></span>
  

