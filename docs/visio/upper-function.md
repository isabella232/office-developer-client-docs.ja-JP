---
title: UPPER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: 大文字に変換された文字列を返します。
ms.openlocfilehash: df8250ef634b04cb19cbb4e120bd02eb77531a82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806728"
---
# <a name="upper-function"></a><span data-ttu-id="d2e3e-103">UPPER 関数</span><span class="sxs-lookup"><span data-stu-id="d2e3e-103">UPPER Function</span></span>

<span data-ttu-id="d2e3e-104">大文字に変換された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d2e3e-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d2e3e-105">構文</span><span class="sxs-lookup"><span data-stu-id="d2e3e-105">Syntax</span></span>

<span data-ttu-id="d2e3e-106">上 (* **式** *)</span><span class="sxs-lookup"><span data-stu-id="d2e3e-106">UPPER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d2e3e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2e3e-107">Parameters</span></span>

|<span data-ttu-id="d2e3e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-108">**Name**</span></span>|<span data-ttu-id="d2e3e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-109">**Required/Optional**</span></span>|<span data-ttu-id="d2e3e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-110">**Data Type**</span></span>|<span data-ttu-id="d2e3e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d2e3e-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="d2e3e-112">_expression_</span></span> <br/> |<span data-ttu-id="d2e3e-113">必須</span><span class="sxs-lookup"><span data-stu-id="d2e3e-113">Required</span></span>  <br/> |<span data-ttu-id="d2e3e-114">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-114">**Varies**</span></span> <br/> | <span data-ttu-id="d2e3e-115">文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、大文字に変換されます。</span><span class="sxs-lookup"><span data-stu-id="d2e3e-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2e3e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d2e3e-116">Remarks</span></span>

<span data-ttu-id="d2e3e-117">大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。</span><span class="sxs-lookup"><span data-stu-id="d2e3e-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d2e3e-118">例</span><span class="sxs-lookup"><span data-stu-id="d2e3e-118">Example</span></span>

<span data-ttu-id="d2e3e-119">UPPER("mIxEd CAse")</span><span class="sxs-lookup"><span data-stu-id="d2e3e-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="d2e3e-120">"MIXED CASE" を返します。</span><span class="sxs-lookup"><span data-stu-id="d2e3e-120">Returns "MIXED CASE".</span></span> 
  

