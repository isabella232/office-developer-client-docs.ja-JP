---
title: PAGENAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: ページ名を文字列として返します。
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339467"
---
# <a name="pagename-function"></a><span data-ttu-id="3059d-103">PAGENAME 関数</span><span class="sxs-lookup"><span data-stu-id="3059d-103">PAGENAME Function</span></span>

<span data-ttu-id="3059d-104">ページ名を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="3059d-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3059d-105">構文</span><span class="sxs-lookup"><span data-stu-id="3059d-105">Syntax</span></span>

<span data-ttu-id="3059d-106">PAGENAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3059d-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3059d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3059d-107">Parameters</span></span>

|<span data-ttu-id="3059d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="3059d-108">**Name**</span></span>|<span data-ttu-id="3059d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3059d-109">**Required/Optional**</span></span>|<span data-ttu-id="3059d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3059d-110">**Data Type**</span></span>|<span data-ttu-id="3059d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3059d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3059d-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="3059d-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="3059d-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="3059d-113">Optional</span></span>  <br/> |<span data-ttu-id="3059d-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="3059d-114">**Number**</span></span> <br/> |<span data-ttu-id="3059d-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="3059d-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3059d-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="3059d-118">Return value</span></span>

<span data-ttu-id="3059d-119">文字列</span><span class="sxs-lookup"><span data-stu-id="3059d-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3059d-120">注釈</span><span class="sxs-lookup"><span data-stu-id="3059d-120">Remarks</span></span>

<span data-ttu-id="3059d-121">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3059d-121">If you pass an illegal language code, the local language is used.</span></span>
  

