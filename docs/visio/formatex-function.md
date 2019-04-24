---
title: FORMATEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: dstUnit で記述された形式に従って書式設定された文字列として、srcUnit で評価された式の結果を返します。
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328631"
---
# <a name="formatex-function"></a><span data-ttu-id="85a1b-103">FORMATEX 関数</span><span class="sxs-lookup"><span data-stu-id="85a1b-103">FORMATEX Function</span></span>

<span data-ttu-id="85a1b-104">dstUnit で記述された形式に従って書式設定された文字列として、srcUnit で評価された式の結果を返します。</span><span class="sxs-lookup"><span data-stu-id="85a1b-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="85a1b-105">構文</span><span class="sxs-lookup"><span data-stu-id="85a1b-105">Syntax</span></span>

<span data-ttu-id="85a1b-106">formatex (\* **式** *、"* **形式** *", [* \* *srcunit* \* *], [* \* *dstunit* \* *], [* \* *langID* \* \*] [, \* \* *calid* \* \*])</span><span class="sxs-lookup"><span data-stu-id="85a1b-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="85a1b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85a1b-107">Parameters</span></span>

|<span data-ttu-id="85a1b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="85a1b-108">**Name**</span></span>|<span data-ttu-id="85a1b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="85a1b-109">**Required/Optional**</span></span>|<span data-ttu-id="85a1b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="85a1b-110">**Data Type**</span></span>|<span data-ttu-id="85a1b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="85a1b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="85a1b-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="85a1b-112">_expression_</span></span> <br/> |<span data-ttu-id="85a1b-113">必須</span><span class="sxs-lookup"><span data-stu-id="85a1b-113">Required</span></span>  <br/> |<span data-ttu-id="85a1b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="85a1b-114">**String**</span></span> <br/> |<span data-ttu-id="85a1b-115">定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。</span><span class="sxs-lookup"><span data-stu-id="85a1b-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="85a1b-116">_format_</span><span class="sxs-lookup"><span data-stu-id="85a1b-116">_format_</span></span> <br/> |<span data-ttu-id="85a1b-117">必須</span><span class="sxs-lookup"><span data-stu-id="85a1b-117">Required</span></span>  <br/> |<span data-ttu-id="85a1b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="85a1b-118">**String**</span></span> <br/> |<span data-ttu-id="85a1b-p101">文字列の書式設定に使用する図の書式設定。図の書式設定の詳細については、「[図の書式設定](about-format-pictures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85a1b-p101">The format picture used to format the string. For more information about format pictures, see [About Format Pictures](about-format-pictures.md).  </span></span><br/> |
| <span data-ttu-id="85a1b-121">_srcunit_</span><span class="sxs-lookup"><span data-stu-id="85a1b-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="85a1b-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="85a1b-122">Optional</span></span>  <br/> |<span data-ttu-id="85a1b-123">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="85a1b-123">**String**</span></span> <br/> | <span data-ttu-id="85a1b-124">式を評価するために使用する単位 (in、cm など) です。</span><span class="sxs-lookup"><span data-stu-id="85a1b-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="85a1b-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="85a1b-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="85a1b-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="85a1b-126">Optional</span></span>  <br/> |<span data-ttu-id="85a1b-127">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="85a1b-127">**String**</span></span> <br/> |<span data-ttu-id="85a1b-128">式の結果に使用する単位 (in、cm など) です。</span><span class="sxs-lookup"><span data-stu-id="85a1b-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="85a1b-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="85a1b-129">_langID_</span></span> <br/> |<span data-ttu-id="85a1b-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="85a1b-130">Optional</span></span>  <br/> |<span data-ttu-id="85a1b-131">**数値**</span><span class="sxs-lookup"><span data-stu-id="85a1b-131">**Number**</span></span> <br/> |<span data-ttu-id="85a1b-132">Microsoft Office system の日付/時間形式の書式設定に使用する言語です。</span><span class="sxs-lookup"><span data-stu-id="85a1b-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="85a1b-133">_calid_</span><span class="sxs-lookup"><span data-stu-id="85a1b-133">_calID_</span></span> <br/> |<span data-ttu-id="85a1b-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="85a1b-134">Optional</span></span>  <br/> |<span data-ttu-id="85a1b-135">**数値**</span><span class="sxs-lookup"><span data-stu-id="85a1b-135">**Number**</span></span> <br/> |<span data-ttu-id="85a1b-136">Microsoft Office system の日付/時間形式を書式設定するときのカレンダーです。</span><span class="sxs-lookup"><span data-stu-id="85a1b-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="85a1b-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="85a1b-137">Return value</span></span>

<span data-ttu-id="85a1b-138">文字列</span><span class="sxs-lookup"><span data-stu-id="85a1b-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85a1b-139">注釈</span><span class="sxs-lookup"><span data-stu-id="85a1b-139">Remarks</span></span>

<span data-ttu-id="85a1b-p102">式の種類および図の書式設定で指定されている形式に応じて、返される文字列の書式が決まります。この書式は式の種類に適したものでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="85a1b-p102">The type of the expression and the type specified in the format picture govern the behavior of the returned string. The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="85a1b-p103">3 + 4 などのように、種類が指定されていない式の結果を計算するには、srcUnit 引数を使用します。3 ft + 8 ft などのように、式の結果の種類が明示されている場合は、srcUnit は無視されます。</span><span class="sxs-lookup"><span data-stu-id="85a1b-p103">The srcUnit argument is used to scale untyped expression results, such as 3 + 4. If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="85a1b-p104">書式設定された結果に使用する単位を指定するには、dstUnit 引数を使用します。dstUnit を指定しないと、式の結果の単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="85a1b-p104">The dstUnit argument is used to specify the units used for the formatted result. If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="85a1b-146">式の結果と書式設定で指定されている形式が異なる場合、書式設定に構文エラーがある場合、または srcUnit や dstUnit として渡された単位が認識されない場合、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="85a1b-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="85a1b-147">例</span><span class="sxs-lookup"><span data-stu-id="85a1b-147">Example</span></span>

<span data-ttu-id="85a1b-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="85a1b-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="85a1b-149">0.18 フィートを返します。</span><span class="sxs-lookup"><span data-stu-id="85a1b-149">Returns 0.18 feet.</span></span> 
  

