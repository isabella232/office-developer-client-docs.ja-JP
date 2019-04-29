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
description: 単語間のスペースを除くすべてのスペースをテキストから削除します。
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435720"
---
# <a name="trim-function"></a><span data-ttu-id="acb48-103">TRIM 関数</span><span class="sxs-lookup"><span data-stu-id="acb48-103">TRIM Function</span></span>

<span data-ttu-id="acb48-104">単語間のスペースを除くすべてのスペースをテキストから削除します。</span><span class="sxs-lookup"><span data-stu-id="acb48-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="acb48-105">構文</span><span class="sxs-lookup"><span data-stu-id="acb48-105">Syntax</span></span>

<span data-ttu-id="acb48-106">TRIM (\* \* *text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="acb48-106">TRIM (\*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="acb48-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="acb48-107">Parameters</span></span>

|<span data-ttu-id="acb48-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="acb48-108">**Name**</span></span>|<span data-ttu-id="acb48-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="acb48-109">**Required/Optional**</span></span>|<span data-ttu-id="acb48-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="acb48-110">**Data Type**</span></span>|<span data-ttu-id="acb48-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="acb48-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="acb48-112">_text_</span><span class="sxs-lookup"><span data-stu-id="acb48-112">_text_</span></span> <br/> |<span data-ttu-id="acb48-113">必須</span><span class="sxs-lookup"><span data-stu-id="acb48-113">Required</span></span>  <br/> |<span data-ttu-id="acb48-114">**String**</span><span class="sxs-lookup"><span data-stu-id="acb48-114">**String**</span></span> <br/> |<span data-ttu-id="acb48-115">空白を削除する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="acb48-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="acb48-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="acb48-116">Return value</span></span>

<span data-ttu-id="acb48-117">文字列</span><span class="sxs-lookup"><span data-stu-id="acb48-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="acb48-118">注釈</span><span class="sxs-lookup"><span data-stu-id="acb48-118">Remarks</span></span>

<span data-ttu-id="acb48-119">他のアプリケーションから渡された文字列に無駄な空白が含まれているような場合に、TRIM 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="acb48-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="acb48-120">例</span><span class="sxs-lookup"><span data-stu-id="acb48-120">Example</span></span>

<span data-ttu-id="acb48-121">TRIM ("January 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="acb48-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="acb48-122">"January 1, 2003" を返します。</span><span class="sxs-lookup"><span data-stu-id="acb48-122">Returns "January 1, 2003".</span></span> 
  

