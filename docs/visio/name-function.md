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
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805914"
---
# <a name="name-function"></a><span data-ttu-id="3943b-103">NAME 関数</span><span class="sxs-lookup"><span data-stu-id="3943b-103">NAME Function</span></span>

<span data-ttu-id="3943b-104">シートの名前を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="3943b-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3943b-105">構文</span><span class="sxs-lookup"><span data-stu-id="3943b-105">Syntax</span></span>

<span data-ttu-id="3943b-106">名 (* * *langID_opt* * *)</span><span class="sxs-lookup"><span data-stu-id="3943b-106">NAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3943b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3943b-107">Parameters</span></span>

|<span data-ttu-id="3943b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="3943b-108">**Name**</span></span>|<span data-ttu-id="3943b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3943b-109">**Required/Optional**</span></span>|<span data-ttu-id="3943b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3943b-110">**Data Type**</span></span>|<span data-ttu-id="3943b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3943b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3943b-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="3943b-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="3943b-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="3943b-113">Optional</span></span>  <br/> |<span data-ttu-id="3943b-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="3943b-114">**Number**</span></span> <br/> |<span data-ttu-id="3943b-p101">関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。</span><span class="sxs-lookup"><span data-stu-id="3943b-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3943b-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="3943b-118">Return value</span></span>

<span data-ttu-id="3943b-119">String</span><span class="sxs-lookup"><span data-stu-id="3943b-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3943b-120">注釈</span><span class="sxs-lookup"><span data-stu-id="3943b-120">Remarks</span></span>

<span data-ttu-id="3943b-121">無効な言語コードを渡した場合、ローカル言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3943b-121">If you pass an illegal language code, the local language is used.</span></span> 
  

