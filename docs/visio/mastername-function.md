---
title: MASTERNAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: シートのマスター シェイプの名前として、文字列を返しますか、シートは、マスターを持っていない場合は、'マスターなし' を文字列を返します。
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805833"
---
# <a name="mastername-function"></a><span data-ttu-id="684f7-103">MASTERNAME 関数</span><span class="sxs-lookup"><span data-stu-id="684f7-103">MASTERNAME Function</span></span>

<span data-ttu-id="684f7-104">シートのマスター シェイプの名前として、文字列を取得または設定の文字列を返します"\<マスターなし\>」シートは、マスターを持っていない場合。</span><span class="sxs-lookup"><span data-stu-id="684f7-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="684f7-105">構文</span><span class="sxs-lookup"><span data-stu-id="684f7-105">Syntax</span></span>

<span data-ttu-id="684f7-106">MASTERNAME ([* * *langID_opt* * *])</span><span class="sxs-lookup"><span data-stu-id="684f7-106">MASTERNAME ([ ** *langID_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="684f7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="684f7-107">Parameters</span></span>

|<span data-ttu-id="684f7-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="684f7-108">**Name**</span></span>|<span data-ttu-id="684f7-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="684f7-109">**Required/Optional**</span></span>|<span data-ttu-id="684f7-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="684f7-110">**Data Type**</span></span>|<span data-ttu-id="684f7-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="684f7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="684f7-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="684f7-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="684f7-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="684f7-113">Optional</span></span>  <br/> |<span data-ttu-id="684f7-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="684f7-114">**Number**</span></span> <br/> |<span data-ttu-id="684f7-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="684f7-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="684f7-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="684f7-118">Return value</span></span>

<span data-ttu-id="684f7-119">String</span><span class="sxs-lookup"><span data-stu-id="684f7-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="684f7-120">注釈</span><span class="sxs-lookup"><span data-stu-id="684f7-120">Remarks</span></span>

<span data-ttu-id="684f7-121">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="684f7-121">If you pass an illegal language code, the local language is used.</span></span> 
  

