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
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804905"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="61a0e-103">BKGPAGENAME 関数</span><span class="sxs-lookup"><span data-stu-id="61a0e-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="61a0e-104">背景ページの名前を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="61a0e-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="61a0e-105">構文</span><span class="sxs-lookup"><span data-stu-id="61a0e-105">Syntax</span></span>

<span data-ttu-id="61a0e-106">BKGPAGENAME (* * *langID_opt* * *)</span><span class="sxs-lookup"><span data-stu-id="61a0e-106">BKGPAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61a0e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="61a0e-107">Parameters</span></span>

|<span data-ttu-id="61a0e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="61a0e-108">**Name**</span></span>|<span data-ttu-id="61a0e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="61a0e-109">**Required/Optional**</span></span>|<span data-ttu-id="61a0e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="61a0e-110">**Data Type**</span></span>|<span data-ttu-id="61a0e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="61a0e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61a0e-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="61a0e-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="61a0e-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="61a0e-113">Optional</span></span>  <br/> |<span data-ttu-id="61a0e-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="61a0e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="61a0e-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="61a0e-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="61a0e-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="61a0e-118">Return value</span></span>

<span data-ttu-id="61a0e-119">String</span><span class="sxs-lookup"><span data-stu-id="61a0e-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61a0e-120">注釈</span><span class="sxs-lookup"><span data-stu-id="61a0e-120">Remarks</span></span>

<span data-ttu-id="61a0e-121">関数を使用してページが背景ページでは、文字列を持っていない場合は、"\<背景なし\>"が返されます。</span><span class="sxs-lookup"><span data-stu-id="61a0e-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="61a0e-122">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="61a0e-122">If you pass an illegal language code, the local language is used.</span></span> 
  

