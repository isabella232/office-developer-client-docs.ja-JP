---
title: LOOKUP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: リスト内のサブ文字列キーの場所を示す 0 から始め、ターゲット文字列に区切り記号が含まれている場合は -1 を返します。
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410330"
---
# <a name="lookup-function"></a><span data-ttu-id="92b4d-103">LOOKUP 関数</span><span class="sxs-lookup"><span data-stu-id="92b4d-103">LOOKUP Function</span></span>

<span data-ttu-id="92b4d-104">リスト内の部分文字列キーの場所を示す 0 から始るインデックスを返し、ターゲット文字列に区切り記号が含まれている場合は -1 を返 _します_。</span><span class="sxs-lookup"><span data-stu-id="92b4d-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="92b4d-105">構文</span><span class="sxs-lookup"><span data-stu-id="92b4d-105">Syntax</span></span>

<span data-ttu-id="92b4d-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *区切* り文字 \*\* "])</span><span class="sxs-lookup"><span data-stu-id="92b4d-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="92b4d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92b4d-107">Parameters</span></span>

|<span data-ttu-id="92b4d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="92b4d-108">**Name**</span></span>|<span data-ttu-id="92b4d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="92b4d-109">**Required/Optional**</span></span>|<span data-ttu-id="92b4d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="92b4d-110">**Data Type**</span></span>|<span data-ttu-id="92b4d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="92b4d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="92b4d-112">_key_</span><span class="sxs-lookup"><span data-stu-id="92b4d-112">_key_</span></span> <br/> |<span data-ttu-id="92b4d-113">必須</span><span class="sxs-lookup"><span data-stu-id="92b4d-113">Required</span></span>  <br/> |<span data-ttu-id="92b4d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="92b4d-114">**String**</span></span> <br/> |<span data-ttu-id="92b4d-115">検索する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="92b4d-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="92b4d-116">_リスト_</span><span class="sxs-lookup"><span data-stu-id="92b4d-116">_list_</span></span> <br/> |<span data-ttu-id="92b4d-117">必須</span><span class="sxs-lookup"><span data-stu-id="92b4d-117">Required</span></span>  <br/> |<span data-ttu-id="92b4d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="92b4d-118">**String**</span></span> <br/> | <span data-ttu-id="92b4d-119">検索するリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="92b4d-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="92b4d-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="92b4d-120">_delimiter_</span></span> <br/> |<span data-ttu-id="92b4d-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="92b4d-121">Optional</span></span>  <br/> |<span data-ttu-id="92b4d-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="92b4d-122">**String**</span></span> <br/> | <span data-ttu-id="92b4d-123">リスト内で区切り文字として使用する  _文字列_ です。</span><span class="sxs-lookup"><span data-stu-id="92b4d-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="92b4d-124">区切  _り文字_ は、長さが 1 文字以上で、マルチバイト文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="92b4d-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="92b4d-125">既定値はセミコロンです。</span><span class="sxs-lookup"><span data-stu-id="92b4d-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="92b4d-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="92b4d-126">Return value</span></span>

<span data-ttu-id="92b4d-127">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="92b4d-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92b4d-128">注釈</span><span class="sxs-lookup"><span data-stu-id="92b4d-128">Remarks</span></span>

<span data-ttu-id="92b4d-p102">LOOKUP 関数による検索では、大文字と小文字は区別されません。リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="92b4d-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="92b4d-p103">すべての引数には、文字列を指定するか、文字列に変換できる式を指定する必要があります。それ以外の引数を指定した場合は、不正な引数が空の文字列に置き換わります。</span><span class="sxs-lookup"><span data-stu-id="92b4d-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="92b4d-134">例 1</span><span class="sxs-lookup"><span data-stu-id="92b4d-134">Example 1</span></span>

<span data-ttu-id="92b4d-135">LOOKUP("rat","cat;rat;;ヤギ")</span><span class="sxs-lookup"><span data-stu-id="92b4d-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="92b4d-136">1 を返します。</span><span class="sxs-lookup"><span data-stu-id="92b4d-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="92b4d-137">例 2</span><span class="sxs-lookup"><span data-stu-id="92b4d-137">Example 2</span></span>

<span data-ttu-id="92b4d-138">LOOKUP("",";cat;rat;;ヤギ")</span><span class="sxs-lookup"><span data-stu-id="92b4d-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="92b4d-139">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="92b4d-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="92b4d-140">例 3</span><span class="sxs-lookup"><span data-stu-id="92b4d-140">Example 3</span></span>

<span data-ttu-id="92b4d-141">LOOKUP("t","cat;rat;;ヤギ","a")</span><span class="sxs-lookup"><span data-stu-id="92b4d-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="92b4d-142">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="92b4d-142">Returns 3.</span></span>
  

