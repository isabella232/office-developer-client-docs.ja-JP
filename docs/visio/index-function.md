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
description: 区切り記号で区切られたリスト内の 0 から始る位置インデックスの部分文字列を返します。 または、インデックスが範囲を外している場合は、空の文字列または errorvalue 引数として指定されたオプションのトークンを返します。
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431576"
---
# <a name="index-function"></a><span data-ttu-id="4ca3f-104">INDEX 関数</span><span class="sxs-lookup"><span data-stu-id="4ca3f-104">INDEX Function</span></span>

<span data-ttu-id="4ca3f-105">区切り記号で区切られたリスト内の 0 から始る位置インデックス _の部分文字列_ を返 _します_。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="4ca3f-106">または、インデックスが範囲を外している場合は、空の文字列または errorvalue 引数として指定されたオプションの  *トークンを返*  します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4ca3f-107">構文</span><span class="sxs-lookup"><span data-stu-id="4ca3f-107">Syntax</span></span>

<span data-ttu-id="4ca3f-108">INDEX(\*\* *index* **," \*\* *list* \*\* "[,** *区切* り文字 \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span><span class="sxs-lookup"><span data-stu-id="4ca3f-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4ca3f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4ca3f-109">Parameters</span></span>

|<span data-ttu-id="4ca3f-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-110">**Name**</span></span>|<span data-ttu-id="4ca3f-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-111">**Required/Optional**</span></span>|<span data-ttu-id="4ca3f-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-112">**Data Type**</span></span>|<span data-ttu-id="4ca3f-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4ca3f-114">_index_</span><span class="sxs-lookup"><span data-stu-id="4ca3f-114">_index_</span></span> <br/> |<span data-ttu-id="4ca3f-115">必須</span><span class="sxs-lookup"><span data-stu-id="4ca3f-115">Required</span></span>  <br/> |<span data-ttu-id="4ca3f-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-116">**Number**</span></span> <br/> |<span data-ttu-id="4ca3f-117">検索する位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="4ca3f-118">_リスト_</span><span class="sxs-lookup"><span data-stu-id="4ca3f-118">_list_</span></span> <br/> |<span data-ttu-id="4ca3f-119">必須</span><span class="sxs-lookup"><span data-stu-id="4ca3f-119">Required</span></span>  <br/> |<span data-ttu-id="4ca3f-120">**String**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-120">**String**</span></span> <br/> |<span data-ttu-id="4ca3f-121">検索するリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="4ca3f-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="4ca3f-122">_delimiter_</span></span> <br/> |<span data-ttu-id="4ca3f-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="4ca3f-123">Optional</span></span>  <br/> |<span data-ttu-id="4ca3f-124">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-124">**String**</span></span> <br/> | <span data-ttu-id="4ca3f-125">リスト内で区切り文字として使用する  _文字列_ です。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="4ca3f-126">区切  _り文字_ は、長さが 1 文字以上で、マルチバイト文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="4ca3f-127">既定値はセミコロンです。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="4ca3f-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="4ca3f-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="4ca3f-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="4ca3f-129">Optional</span></span>  <br/> |<span data-ttu-id="4ca3f-130">**数値**</span><span class="sxs-lookup"><span data-stu-id="4ca3f-130">**Number**</span></span> <br/> | <span data-ttu-id="4ca3f-p104">インデックスが範囲外の場合に返す、ユーザー指定の値です。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ca3f-133">注釈</span><span class="sxs-lookup"><span data-stu-id="4ca3f-133">Remarks</span></span>

<span data-ttu-id="4ca3f-p105">リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="4ca3f-136">インデックスが範囲を外している場合、Visio引数 errorvalue として指定された空の文字列またはオプションの *トークンを返* します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4ca3f-137">例 1</span><span class="sxs-lookup"><span data-stu-id="4ca3f-137">Example 1</span></span>

<span data-ttu-id="4ca3f-138">INDEX(3,"cat;rat;;ヤギ")</span><span class="sxs-lookup"><span data-stu-id="4ca3f-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="4ca3f-139">"goat" を返します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4ca3f-140">例 2</span><span class="sxs-lookup"><span data-stu-id="4ca3f-140">Example 2</span></span>

<span data-ttu-id="4ca3f-141">INDEX(54,";1;2;3;",,"ERROR")</span><span class="sxs-lookup"><span data-stu-id="4ca3f-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="4ca3f-142">"ERROR" を返します。</span><span class="sxs-lookup"><span data-stu-id="4ca3f-142">Returns "ERROR".</span></span>
  

