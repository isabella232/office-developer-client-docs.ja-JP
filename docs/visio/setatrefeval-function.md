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
description: SETATREF 関数の式のパラメーターで使用すると、SETATREF 参照パラメーターに割り当てる前にその式を評価するかを指定します。
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806366"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="8b577-103">SETATREFEVAL 関数</span><span class="sxs-lookup"><span data-stu-id="8b577-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="8b577-104">SETATREF 関数の_式_のパラメーターで使用すると、SETATREF_参照_パラメーターに割り当てる前にその_式_を評価するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8b577-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8b577-105">構文</span><span class="sxs-lookup"><span data-stu-id="8b577-105">Syntax</span></span>

<span data-ttu-id="8b577-106">SETATREFEVAL (* * *expr* * *)</span><span class="sxs-lookup"><span data-stu-id="8b577-106">SETATREFEVAL(** *expr* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8b577-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b577-107">Parameters</span></span>

|<span data-ttu-id="8b577-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="8b577-108">**Name**</span></span>|<span data-ttu-id="8b577-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="8b577-109">**Required/Optional**</span></span>|<span data-ttu-id="8b577-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="8b577-110">**Data Type**</span></span>|<span data-ttu-id="8b577-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b577-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8b577-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="8b577-112">_expr_</span></span> <br/> |<span data-ttu-id="8b577-113">必須</span><span class="sxs-lookup"><span data-stu-id="8b577-113">Required</span></span>  <br/> |<span data-ttu-id="8b577-114">**多様**</span><span class="sxs-lookup"><span data-stu-id="8b577-114">**Varies**</span></span> <br/> | <span data-ttu-id="8b577-115">SETATREF 関数は、_セット式_を別のセルにリダイレクトするときに評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b577-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b577-116">注釈</span><span class="sxs-lookup"><span data-stu-id="8b577-116">Remarks</span></span>

<span data-ttu-id="8b577-117">SETATREF 関数の*式*のパラメーターを参照先のセルに代入すると、Microsoft Visio に書き込みます*セット式*セル式としてデフォルトで。</span><span class="sxs-lookup"><span data-stu-id="8b577-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="8b577-118">ただし、*セット式*のパラメーターの任意の部分は、SETATREFEVAL 関数によってラップされたが、Visio は式を評価し、SETATREF 式を解決する前にその結果で SETATREFEVAL 関数を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8b577-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8b577-119">例</span><span class="sxs-lookup"><span data-stu-id="8b577-119">Example</span></span>

<span data-ttu-id="8b577-120">例については、[SETATREF](setatref-function.md) 関数を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b577-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

