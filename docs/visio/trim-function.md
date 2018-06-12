---
title: TRIM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: 単語間のスペースを 1 つ残して、テキストからすべての空白を削除します。
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806696"
---
# <a name="trim-function"></a><span data-ttu-id="41ebb-103">TRIM 関数</span><span class="sxs-lookup"><span data-stu-id="41ebb-103">TRIM Function</span></span>

<span data-ttu-id="41ebb-104">単語間のスペースを 1 つ残して、テキストからすべての空白を削除します。</span><span class="sxs-lookup"><span data-stu-id="41ebb-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="41ebb-105">構文</span><span class="sxs-lookup"><span data-stu-id="41ebb-105">Syntax</span></span>

<span data-ttu-id="41ebb-106">トリミング (* **テキスト** *)</span><span class="sxs-lookup"><span data-stu-id="41ebb-106">TRIM (** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="41ebb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="41ebb-107">Parameters</span></span>

|<span data-ttu-id="41ebb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="41ebb-108">**Name**</span></span>|<span data-ttu-id="41ebb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="41ebb-109">**Required/Optional**</span></span>|<span data-ttu-id="41ebb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="41ebb-110">**Data Type**</span></span>|<span data-ttu-id="41ebb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="41ebb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="41ebb-112">_text_</span><span class="sxs-lookup"><span data-stu-id="41ebb-112">_text_</span></span> <br/> |<span data-ttu-id="41ebb-113">必須</span><span class="sxs-lookup"><span data-stu-id="41ebb-113">Required</span></span>  <br/> |<span data-ttu-id="41ebb-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="41ebb-114">**String**</span></span> <br/> |<span data-ttu-id="41ebb-115">空白を削除する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="41ebb-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="41ebb-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="41ebb-116">Return value</span></span>

<span data-ttu-id="41ebb-117">文字列</span><span class="sxs-lookup"><span data-stu-id="41ebb-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41ebb-118">注釈</span><span class="sxs-lookup"><span data-stu-id="41ebb-118">Remarks</span></span>

<span data-ttu-id="41ebb-119">他のアプリケーションから渡された文字列に無駄な空白が含まれているような場合に、TRIM 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="41ebb-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="41ebb-120">例</span><span class="sxs-lookup"><span data-stu-id="41ebb-120">Example</span></span>

<span data-ttu-id="41ebb-121">トリム (「2003 年 1 月 1日」)</span><span class="sxs-lookup"><span data-stu-id="41ebb-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="41ebb-122">"January 1, 2003" を返します。</span><span class="sxs-lookup"><span data-stu-id="41ebb-122">Returns "January 1, 2003".</span></span> 
  
