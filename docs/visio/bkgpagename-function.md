---
title: BKGPAGENAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: 背景ページの名前を文字列として返します。
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358542"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="fa199-103">BKGPAGENAME 関数</span><span class="sxs-lookup"><span data-stu-id="fa199-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="fa199-104">背景ページの名前を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="fa199-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fa199-105">構文</span><span class="sxs-lookup"><span data-stu-id="fa199-105">Syntax</span></span>

<span data-ttu-id="fa199-106">BKGPAGENAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fa199-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fa199-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa199-107">Parameters</span></span>

|<span data-ttu-id="fa199-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="fa199-108">**Name**</span></span>|<span data-ttu-id="fa199-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fa199-109">**Required/Optional**</span></span>|<span data-ttu-id="fa199-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fa199-110">**Data Type**</span></span>|<span data-ttu-id="fa199-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fa199-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fa199-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="fa199-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="fa199-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="fa199-113">Optional</span></span>  <br/> |<span data-ttu-id="fa199-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="fa199-114">**Numeric**</span></span> <br/> |<span data-ttu-id="fa199-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="fa199-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fa199-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa199-118">Return value</span></span>

<span data-ttu-id="fa199-119">文字列</span><span class="sxs-lookup"><span data-stu-id="fa199-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa199-120">注釈</span><span class="sxs-lookup"><span data-stu-id="fa199-120">Remarks</span></span>

<span data-ttu-id="fa199-121">関数を使用しているページに背景ページがない場合は、"\<背景\>なし" という文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="fa199-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="fa199-122">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa199-122">If you pass an illegal language code, the local language is used.</span></span> 
  

