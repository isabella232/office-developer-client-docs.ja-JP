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
description: 区切り記号で区切られたリスト内の位置を示す 0 から始まるインデックス位置の部分文字列を返します。 または、インデックスが範囲を返しますが空の文字列、または errorvalue 引数として提供されている場合。
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805575"
---
# <a name="index-function"></a><span data-ttu-id="43528-104">INDEX 関数</span><span class="sxs-lookup"><span data-stu-id="43528-104">INDEX Function</span></span>

<span data-ttu-id="43528-105">_区切り記号_で区切られた_リスト_内の位置の 0 から始まる_インデックス_位置の部分文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="43528-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="43528-106">または、インデックスが範囲を返しますが空の文字列、または*errorvalue*引数として提供されている場合。</span><span class="sxs-lookup"><span data-stu-id="43528-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="43528-107">構文</span><span class="sxs-lookup"><span data-stu-id="43528-107">Syntax</span></span>

<span data-ttu-id="43528-108">インデックス (* **インデックス** *、"* **リスト** *] [、[* **区切り記号** *] [、[* * *errorvalue* * *]])</span><span class="sxs-lookup"><span data-stu-id="43528-108">INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="43528-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="43528-109">Parameters</span></span>

|<span data-ttu-id="43528-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="43528-110">**Name**</span></span>|<span data-ttu-id="43528-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="43528-111">**Required/Optional**</span></span>|<span data-ttu-id="43528-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="43528-112">**Data Type**</span></span>|<span data-ttu-id="43528-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="43528-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="43528-114">_index_</span><span class="sxs-lookup"><span data-stu-id="43528-114">_index_</span></span> <br/> |<span data-ttu-id="43528-115">必須</span><span class="sxs-lookup"><span data-stu-id="43528-115">Required</span></span>  <br/> |<span data-ttu-id="43528-116">**番号**</span><span class="sxs-lookup"><span data-stu-id="43528-116">**Number**</span></span> <br/> |<span data-ttu-id="43528-117">検索する位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="43528-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="43528-118">_リスト_</span><span class="sxs-lookup"><span data-stu-id="43528-118">_list_</span></span> <br/> |<span data-ttu-id="43528-119">必須</span><span class="sxs-lookup"><span data-stu-id="43528-119">Required</span></span>  <br/> |<span data-ttu-id="43528-120">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="43528-120">**String**</span></span> <br/> |<span data-ttu-id="43528-121">検索するリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="43528-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="43528-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="43528-122">_delimiter_</span></span> <br/> |<span data-ttu-id="43528-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="43528-123">Optional</span></span>  <br/> |<span data-ttu-id="43528-124">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="43528-124">**String**</span></span> <br/> | <span data-ttu-id="43528-125">_リスト_内の区切り文字として使用する文字列です。</span><span class="sxs-lookup"><span data-stu-id="43528-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="43528-126">_区切り記号_文字列は、1 つ以上の文字し、マルチバイト文字が含まれます。</span><span class="sxs-lookup"><span data-stu-id="43528-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="43528-127">既定値は、セミコロンです。</span><span class="sxs-lookup"><span data-stu-id="43528-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="43528-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="43528-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="43528-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="43528-129">Optional</span></span>  <br/> |<span data-ttu-id="43528-130">**番号**</span><span class="sxs-lookup"><span data-stu-id="43528-130">**Number**</span></span> <br/> | <span data-ttu-id="43528-p104">インデックスが範囲外の場合に返す、ユーザー指定の値です。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="43528-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43528-133">注釈</span><span class="sxs-lookup"><span data-stu-id="43528-133">Remarks</span></span>

<span data-ttu-id="43528-p105">リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="43528-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="43528-136">インデックスが範囲外にある場合は、Visio は、空の文字列、または*errorvalue*引数として指定された省略可能なトークンを返します。</span><span class="sxs-lookup"><span data-stu-id="43528-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="43528-137">例 1</span><span class="sxs-lookup"><span data-stu-id="43528-137">Example 1</span></span>

<span data-ttu-id="43528-138">INDEX(3,"cat;rat;;goat")</span><span class="sxs-lookup"><span data-stu-id="43528-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="43528-139">"goat" を返します。</span><span class="sxs-lookup"><span data-stu-id="43528-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="43528-140">例 2</span><span class="sxs-lookup"><span data-stu-id="43528-140">Example 2</span></span>

<span data-ttu-id="43528-141">INDEX(54,";1;2;3;",,"ERROR")</span><span class="sxs-lookup"><span data-stu-id="43528-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="43528-142">「エラー」を返します。</span><span class="sxs-lookup"><span data-stu-id="43528-142">Returns "ERROR".</span></span>
  

