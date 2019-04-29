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
description: シートのマスターシェイプ名を文字列として返します。または、シートにマスターシェイプがない場合は、文字列 ' master ' を返します。
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414754"
---
# <a name="mastername-function"></a><span data-ttu-id="ed9d0-103">MASTERNAME 関数</span><span class="sxs-lookup"><span data-stu-id="ed9d0-103">MASTERNAME Function</span></span>

<span data-ttu-id="ed9d0-104">シートのマスターシェイプ名を文字列として返します。または\<、シート\>にマスターシェイプがない場合は、文字列 "master" を返します。</span><span class="sxs-lookup"><span data-stu-id="ed9d0-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ed9d0-105">構文</span><span class="sxs-lookup"><span data-stu-id="ed9d0-105">Syntax</span></span>

<span data-ttu-id="ed9d0-106">mastername ([\* \* *langID_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="ed9d0-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed9d0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ed9d0-107">Parameters</span></span>

|<span data-ttu-id="ed9d0-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ed9d0-108">**Name**</span></span>|<span data-ttu-id="ed9d0-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ed9d0-109">**Required/Optional**</span></span>|<span data-ttu-id="ed9d0-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ed9d0-110">**Data Type**</span></span>|<span data-ttu-id="ed9d0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ed9d0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed9d0-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="ed9d0-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="ed9d0-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="ed9d0-113">Optional</span></span>  <br/> |<span data-ttu-id="ed9d0-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="ed9d0-114">**Number**</span></span> <br/> |<span data-ttu-id="ed9d0-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="ed9d0-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ed9d0-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="ed9d0-118">Return value</span></span>

<span data-ttu-id="ed9d0-119">文字列</span><span class="sxs-lookup"><span data-stu-id="ed9d0-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed9d0-120">注釈</span><span class="sxs-lookup"><span data-stu-id="ed9d0-120">Remarks</span></span>

<span data-ttu-id="ed9d0-121">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed9d0-121">If you pass an illegal language code, the local language is used.</span></span> 
  

