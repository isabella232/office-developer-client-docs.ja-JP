---
title: SETATREFEVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: SETATREF 関数の set_expression パラメーターで使用され、SETATREF の reference パラメーターに割り当てる前に set_expression を評価する必要があることを示します。
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432983"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="5ef41-103">SETATREFEVAL 関数</span><span class="sxs-lookup"><span data-stu-id="5ef41-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="5ef41-104">SETATREF 関数の_set_expression_パラメーターで使用され、SETATREF の_reference_パラメーターに割り当てる前に_set_expression_を評価する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="5ef41-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5ef41-105">構文</span><span class="sxs-lookup"><span data-stu-id="5ef41-105">Syntax</span></span>

<span data-ttu-id="5ef41-106">SETATREFEVAL (\* \* *expr* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5ef41-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ef41-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ef41-107">Parameters</span></span>

|<span data-ttu-id="5ef41-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5ef41-108">**Name**</span></span>|<span data-ttu-id="5ef41-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5ef41-109">**Required/Optional**</span></span>|<span data-ttu-id="5ef41-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5ef41-110">**Data Type**</span></span>|<span data-ttu-id="5ef41-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ef41-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ef41-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="5ef41-112">_expr_</span></span> <br/> |<span data-ttu-id="5ef41-113">必須</span><span class="sxs-lookup"><span data-stu-id="5ef41-113">Required</span></span>  <br/> |<span data-ttu-id="5ef41-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="5ef41-114">**Varies**</span></span> <br/> | <span data-ttu-id="5ef41-115">SETATREF 関数が_set_expression_を別のセルにリダイレクトするときに評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ef41-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ef41-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5ef41-116">Remarks</span></span>

<span data-ttu-id="5ef41-117">SETATREF 関数の*set_expression*パラメーターを参照先のセルに代入すると、Microsoft Visio は既定でそのセルに*set_expression*を式として書き込みます。</span><span class="sxs-lookup"><span data-stu-id="5ef41-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="5ef41-118">ただし、 *set_expression*パラメーターのいずれかの部分が SETATREFEVAL 関数によってラップされている場合、Visio は式を評価し、SETATREFEVAL 関数をその結果に置き換えて SETATREF 式を解決します。</span><span class="sxs-lookup"><span data-stu-id="5ef41-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5ef41-119">例</span><span class="sxs-lookup"><span data-stu-id="5ef41-119">Example</span></span>

<span data-ttu-id="5ef41-120">例については、[SETATREF](setatref-function.md) 関数を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ef41-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

