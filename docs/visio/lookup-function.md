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
description: リスト内の部分文字列のキーの場所または対象の文字列に区切り文字が含まれている場合は-1 を返しますを示す 0 から始まるインデックスを返します。
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805800"
---
# <a name="lookup-function"></a><span data-ttu-id="4ccee-103">LOOKUP 関数</span><span class="sxs-lookup"><span data-stu-id="4ccee-103">LOOKUP Function</span></span>

<span data-ttu-id="4ccee-104">_リスト_内の部分文字列_キー_の場所または対象の文字列に_区切り記号_が含まれている場合は-1 を返しますを示す 0 から始まるインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4ccee-105">構文</span><span class="sxs-lookup"><span data-stu-id="4ccee-105">Syntax</span></span>

<span data-ttu-id="4ccee-106">参照 ("* **キー* * *」、「* **リスト** * [、* **区切り記号** *」])</span><span class="sxs-lookup"><span data-stu-id="4ccee-106">LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4ccee-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4ccee-107">Parameters</span></span>

|<span data-ttu-id="4ccee-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="4ccee-108">**Name**</span></span>|<span data-ttu-id="4ccee-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4ccee-109">**Required/Optional**</span></span>|<span data-ttu-id="4ccee-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4ccee-110">**Data Type**</span></span>|<span data-ttu-id="4ccee-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ccee-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4ccee-112">_キー_</span><span class="sxs-lookup"><span data-stu-id="4ccee-112">_key_</span></span> <br/> |<span data-ttu-id="4ccee-113">必須</span><span class="sxs-lookup"><span data-stu-id="4ccee-113">Required</span></span>  <br/> |<span data-ttu-id="4ccee-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4ccee-114">**String**</span></span> <br/> |<span data-ttu-id="4ccee-115">検索する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="4ccee-116">_リスト_</span><span class="sxs-lookup"><span data-stu-id="4ccee-116">_list_</span></span> <br/> |<span data-ttu-id="4ccee-117">必須</span><span class="sxs-lookup"><span data-stu-id="4ccee-117">Required</span></span>  <br/> |<span data-ttu-id="4ccee-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4ccee-118">**String**</span></span> <br/> | <span data-ttu-id="4ccee-119">検索するリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="4ccee-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="4ccee-120">_delimiter_</span></span> <br/> |<span data-ttu-id="4ccee-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="4ccee-121">Optional</span></span>  <br/> |<span data-ttu-id="4ccee-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4ccee-122">**String**</span></span> <br/> | <span data-ttu-id="4ccee-123">_リスト_内の区切り文字として使用する文字列です。</span><span class="sxs-lookup"><span data-stu-id="4ccee-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="4ccee-124">_区切り記号_文字列は 1 文字以上の長さし、マルチバイト文字を含めることがあります。</span><span class="sxs-lookup"><span data-stu-id="4ccee-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="4ccee-125">既定値は、セミコロンです。</span><span class="sxs-lookup"><span data-stu-id="4ccee-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4ccee-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4ccee-126">Return value</span></span>

<span data-ttu-id="4ccee-127">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="4ccee-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ccee-128">注釈</span><span class="sxs-lookup"><span data-stu-id="4ccee-128">Remarks</span></span>

<span data-ttu-id="4ccee-p102">LOOKUP 関数による検索では、大文字と小文字は区別されません。リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="4ccee-p103">すべての引数には、文字列を指定するか、文字列に変換できる式を指定する必要があります。それ以外の引数を指定した場合は、不正な引数が空の文字列に置き換わります。</span><span class="sxs-lookup"><span data-stu-id="4ccee-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4ccee-134">例 1</span><span class="sxs-lookup"><span data-stu-id="4ccee-134">Example 1</span></span>

<span data-ttu-id="4ccee-135">LOOKUP("rat","cat;rat;;goat")</span><span class="sxs-lookup"><span data-stu-id="4ccee-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="4ccee-136">1 を返します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4ccee-137">例 2</span><span class="sxs-lookup"><span data-stu-id="4ccee-137">Example 2</span></span>

<span data-ttu-id="4ccee-138">LOOKUP("",";cat;rat;;goat")</span><span class="sxs-lookup"><span data-stu-id="4ccee-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="4ccee-139">0 を返します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4ccee-140">例 3</span><span class="sxs-lookup"><span data-stu-id="4ccee-140">Example 3</span></span>

<span data-ttu-id="4ccee-141">LOOKUP("t","cat;rat;;goat","a")</span><span class="sxs-lookup"><span data-stu-id="4ccee-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="4ccee-142">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="4ccee-142">Returns 3.</span></span>
  

