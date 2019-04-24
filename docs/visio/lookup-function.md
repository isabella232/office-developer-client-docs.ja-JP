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
description: リスト内のサブ文字列キーの位置を示す0から始まるインデックスを返します。または、対象の文字列に区切り文字が含まれている場合は-1 を返します。
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358031"
---
# <a name="lookup-function"></a><span data-ttu-id="ea9cf-103">LOOKUP 関数</span><span class="sxs-lookup"><span data-stu-id="ea9cf-103">LOOKUP Function</span></span>

<span data-ttu-id="ea9cf-104">_リスト_内のサブ文字列_キー_の位置を示す0から始まるインデックスを返します。または、対象の文字列に_区切り文字_が含まれている場合は-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ea9cf-105">構文</span><span class="sxs-lookup"><span data-stu-id="ea9cf-105">Syntax</span></span>

<span data-ttu-id="ea9cf-106">LOOKUP ("\* \* *key* \* *", "* \* *list* \* *" [, "* \* *delimiter* \* \*")</span><span class="sxs-lookup"><span data-stu-id="ea9cf-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ea9cf-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ea9cf-107">Parameters</span></span>

|<span data-ttu-id="ea9cf-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-108">**Name**</span></span>|<span data-ttu-id="ea9cf-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-109">**Required/Optional**</span></span>|<span data-ttu-id="ea9cf-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-110">**Data Type**</span></span>|<span data-ttu-id="ea9cf-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ea9cf-112">_key_</span><span class="sxs-lookup"><span data-stu-id="ea9cf-112">_key_</span></span> <br/> |<span data-ttu-id="ea9cf-113">必須</span><span class="sxs-lookup"><span data-stu-id="ea9cf-113">Required</span></span>  <br/> |<span data-ttu-id="ea9cf-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-114">**String**</span></span> <br/> |<span data-ttu-id="ea9cf-115">検索する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="ea9cf-116">_リスト_</span><span class="sxs-lookup"><span data-stu-id="ea9cf-116">_list_</span></span> <br/> |<span data-ttu-id="ea9cf-117">必須</span><span class="sxs-lookup"><span data-stu-id="ea9cf-117">Required</span></span>  <br/> |<span data-ttu-id="ea9cf-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-118">**String**</span></span> <br/> | <span data-ttu-id="ea9cf-119">検索するリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="ea9cf-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="ea9cf-120">_delimiter_</span></span> <br/> |<span data-ttu-id="ea9cf-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="ea9cf-121">Optional</span></span>  <br/> |<span data-ttu-id="ea9cf-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="ea9cf-122">**String**</span></span> <br/> | <span data-ttu-id="ea9cf-123">_リスト_内で区切り文字として使用する文字列。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="ea9cf-124">_区切り_文字には、複数の文字の長さを指定できます。また、マルチバイト文字を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="ea9cf-125">既定値はセミコロンです。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ea9cf-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="ea9cf-126">Return value</span></span>

<span data-ttu-id="ea9cf-127">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="ea9cf-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea9cf-128">解説</span><span class="sxs-lookup"><span data-stu-id="ea9cf-128">Remarks</span></span>

<span data-ttu-id="ea9cf-p102">LOOKUP 関数による検索では、大文字と小文字は区別されません。リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="ea9cf-p103">すべての引数には、文字列を指定するか、文字列に変換できる式を指定する必要があります。それ以外の引数を指定した場合は、不正な引数が空の文字列に置き換わります。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ea9cf-134">例 1</span><span class="sxs-lookup"><span data-stu-id="ea9cf-134">Example 1</span></span>

<span data-ttu-id="ea9cf-135">参照 ("rat", "cat; rat;;goat ")</span><span class="sxs-lookup"><span data-stu-id="ea9cf-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="ea9cf-136">1 を返します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ea9cf-137">例 2</span><span class="sxs-lookup"><span data-stu-id="ea9cf-137">Example 2</span></span>

<span data-ttu-id="ea9cf-138">LOOKUP ("", "; cat; rat;;goat ")</span><span class="sxs-lookup"><span data-stu-id="ea9cf-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="ea9cf-139">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ea9cf-140">例 3</span><span class="sxs-lookup"><span data-stu-id="ea9cf-140">Example 3</span></span>

<span data-ttu-id="ea9cf-141">LOOKUP ("t", "cat; rat;;goat "," a ")</span><span class="sxs-lookup"><span data-stu-id="ea9cf-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="ea9cf-142">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="ea9cf-142">Returns 3.</span></span>
  

