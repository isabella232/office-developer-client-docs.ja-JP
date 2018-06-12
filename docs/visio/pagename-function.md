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
ms.openlocfilehash: 530707530d60955f460d6a747024b98ebdd5ab62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805967"
---
# <a name="pagename-function"></a><span data-ttu-id="dba5a-103">PAGENAME 関数</span><span class="sxs-lookup"><span data-stu-id="dba5a-103">PAGENAME Function</span></span>

<span data-ttu-id="dba5a-104">ページ名を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="dba5a-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dba5a-105">構文</span><span class="sxs-lookup"><span data-stu-id="dba5a-105">Syntax</span></span>

<span data-ttu-id="dba5a-106">指定した PAGENAME (* * *langID_opt* * *)</span><span class="sxs-lookup"><span data-stu-id="dba5a-106">PAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dba5a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="dba5a-107">Parameters</span></span>

|<span data-ttu-id="dba5a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="dba5a-108">**Name**</span></span>|<span data-ttu-id="dba5a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dba5a-109">**Required/Optional**</span></span>|<span data-ttu-id="dba5a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dba5a-110">**Data Type**</span></span>|<span data-ttu-id="dba5a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="dba5a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dba5a-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="dba5a-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="dba5a-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="dba5a-113">Optional</span></span>  <br/> |<span data-ttu-id="dba5a-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="dba5a-114">**Number**</span></span> <br/> |<span data-ttu-id="dba5a-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="dba5a-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dba5a-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dba5a-118">Return value</span></span>

<span data-ttu-id="dba5a-119">文字列</span><span class="sxs-lookup"><span data-stu-id="dba5a-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dba5a-120">注釈</span><span class="sxs-lookup"><span data-stu-id="dba5a-120">Remarks</span></span>

<span data-ttu-id="dba5a-121">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="dba5a-121">If you pass an illegal language code, the local language is used.</span></span>
  

