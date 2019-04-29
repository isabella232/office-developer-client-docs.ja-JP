---
title: INDEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: 区切り文字で区切られた、リスト内の0から始まるインデックス位置にあるサブ文字列を返します。 または、インデックスが範囲外の場合は、空の文字列または errorvalue 引数として指定されたオプションのトークンを返します。
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431576"
---
# <a name="index-function"></a><span data-ttu-id="4e3fb-104">INDEX 関数</span><span class="sxs-lookup"><span data-stu-id="4e3fb-104">INDEX Function</span></span>

<span data-ttu-id="4e3fb-105">_区切り文字_で区切られた、_リスト_内の0から始まる_インデックス_位置にあるサブ文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="4e3fb-106">または、インデックスが範囲外の場合は、空の文字列または*errorvalue*引数として指定されたオプションのトークンを返します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4e3fb-107">構文</span><span class="sxs-lookup"><span data-stu-id="4e3fb-107">Syntax</span></span>

<span data-ttu-id="4e3fb-108">index (\* \* *index* \* *、"* \* *list* \* *" [, [* **区切り文字** *] [, [* \* *errorvalue* \* \*]])</span><span class="sxs-lookup"><span data-stu-id="4e3fb-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e3fb-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4e3fb-109">Parameters</span></span>

|<span data-ttu-id="4e3fb-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-110">**Name**</span></span>|<span data-ttu-id="4e3fb-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-111">**Required/Optional**</span></span>|<span data-ttu-id="4e3fb-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-112">**Data Type**</span></span>|<span data-ttu-id="4e3fb-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e3fb-114">_index_</span><span class="sxs-lookup"><span data-stu-id="4e3fb-114">_index_</span></span> <br/> |<span data-ttu-id="4e3fb-115">必須</span><span class="sxs-lookup"><span data-stu-id="4e3fb-115">Required</span></span>  <br/> |<span data-ttu-id="4e3fb-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-116">**Number**</span></span> <br/> |<span data-ttu-id="4e3fb-117">検索する位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="4e3fb-118">_list_</span><span class="sxs-lookup"><span data-stu-id="4e3fb-118">_list_</span></span> <br/> |<span data-ttu-id="4e3fb-119">必須</span><span class="sxs-lookup"><span data-stu-id="4e3fb-119">Required</span></span>  <br/> |<span data-ttu-id="4e3fb-120">**String**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-120">**String**</span></span> <br/> |<span data-ttu-id="4e3fb-121">検索するリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="4e3fb-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="4e3fb-122">_delimiter_</span></span> <br/> |<span data-ttu-id="4e3fb-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="4e3fb-123">Optional</span></span>  <br/> |<span data-ttu-id="4e3fb-124">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-124">**String**</span></span> <br/> | <span data-ttu-id="4e3fb-125">_リスト_内で区切り文字として使用する文字列。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="4e3fb-126">_デリミター_文字列には、長さが複数の文字を使用でき、マルチバイト文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="4e3fb-127">既定値はセミコロンです。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="4e3fb-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="4e3fb-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="4e3fb-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="4e3fb-129">Optional</span></span>  <br/> |<span data-ttu-id="4e3fb-130">**数値**</span><span class="sxs-lookup"><span data-stu-id="4e3fb-130">**Number**</span></span> <br/> | <span data-ttu-id="4e3fb-131">インデックスが範囲外の場合に返す、ユーザー指定の値です。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="4e3fb-132">既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e3fb-133">注釈</span><span class="sxs-lookup"><span data-stu-id="4e3fb-133">Remarks</span></span>

<span data-ttu-id="4e3fb-p105">リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="4e3fb-136">インデックスが範囲外の場合、Visio は空の文字列または*errorvalue*引数として指定されたオプションのトークンを返します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4e3fb-137">例 1</span><span class="sxs-lookup"><span data-stu-id="4e3fb-137">Example 1</span></span>

<span data-ttu-id="4e3fb-138">インデックス (3, "cat; rat;;goat ")</span><span class="sxs-lookup"><span data-stu-id="4e3fb-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="4e3fb-139">"goat" を返します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4e3fb-140">例 2</span><span class="sxs-lookup"><span data-stu-id="4e3fb-140">Example 2</span></span>

<span data-ttu-id="4e3fb-141">インデックス (54, "; 1; 2; 3;",, "ERROR")</span><span class="sxs-lookup"><span data-stu-id="4e3fb-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="4e3fb-142">"ERROR" を返します。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-142">Returns "ERROR".</span></span>
  

