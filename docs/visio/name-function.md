---
title: NAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: シートの名前を文字列として返します。
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319426"
---
# <a name="name-function"></a><span data-ttu-id="bc78a-103">NAME 関数</span><span class="sxs-lookup"><span data-stu-id="bc78a-103">NAME Function</span></span>

<span data-ttu-id="bc78a-104">シートの名前を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="bc78a-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bc78a-105">構文</span><span class="sxs-lookup"><span data-stu-id="bc78a-105">Syntax</span></span>

<span data-ttu-id="bc78a-106">NAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="bc78a-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bc78a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc78a-107">Parameters</span></span>

|<span data-ttu-id="bc78a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="bc78a-108">**Name**</span></span>|<span data-ttu-id="bc78a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="bc78a-109">**Required/Optional**</span></span>|<span data-ttu-id="bc78a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="bc78a-110">**Data Type**</span></span>|<span data-ttu-id="bc78a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="bc78a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bc78a-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="bc78a-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="bc78a-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="bc78a-113">Optional</span></span>  <br/> |<span data-ttu-id="bc78a-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="bc78a-114">**Number**</span></span> <br/> |<span data-ttu-id="bc78a-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc78a-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bc78a-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="bc78a-118">Return value</span></span>

<span data-ttu-id="bc78a-119">文字列</span><span class="sxs-lookup"><span data-stu-id="bc78a-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc78a-120">注釈</span><span class="sxs-lookup"><span data-stu-id="bc78a-120">Remarks</span></span>

<span data-ttu-id="bc78a-121">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc78a-121">If you pass an illegal language code, the local language is used.</span></span> 
  

