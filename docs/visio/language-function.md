---
title: LANGUAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: さまざまな言語表現との間の比較演算を使用できます。 ロケール id (LCID) の値をインターネット技術標準化委員会言語タグ (BCP 47) の値を変換するためには適しています。
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805675"
---
# <a name="language-function"></a><span data-ttu-id="7d27d-104">LANGUAGE 関数</span><span class="sxs-lookup"><span data-stu-id="7d27d-104">LANGUAGE Function</span></span>

<span data-ttu-id="7d27d-105">さまざまな言語表現との間の比較演算を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d27d-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="7d27d-106">ロケール id (LCID) の値をインターネット技術標準化委員会言語タグ (BCP 47) の値を変換するためには適しています。</span><span class="sxs-lookup"><span data-stu-id="7d27d-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7d27d-107">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="7d27d-107">Version Information</span></span>

<span data-ttu-id="7d27d-108">Visio 2013 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="7d27d-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7d27d-109">構文</span><span class="sxs-lookup"><span data-stu-id="7d27d-109">Syntax</span></span>

 <span data-ttu-id="7d27d-110">**言語**( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="7d27d-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="7d27d-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d27d-111">Parameters</span></span>

|<span data-ttu-id="7d27d-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="7d27d-112">**Name**</span></span>|<span data-ttu-id="7d27d-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="7d27d-113">**Required/Optional**</span></span>|<span data-ttu-id="7d27d-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="7d27d-114">**Data Type**</span></span>|<span data-ttu-id="7d27d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="7d27d-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7d27d-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="7d27d-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="7d27d-117">必須</span><span class="sxs-lookup"><span data-stu-id="7d27d-117">Required</span></span>  <br/> |<span data-ttu-id="7d27d-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="7d27d-118">**String**</span></span> <br/> |<span data-ttu-id="7d27d-119">言語の LCID または BCP 47 の値です。</span><span class="sxs-lookup"><span data-stu-id="7d27d-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="7d27d-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7d27d-120">Return value</span></span>

<span data-ttu-id="7d27d-121">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="7d27d-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="7d27d-122">例</span><span class="sxs-lookup"><span data-stu-id="7d27d-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="7d27d-123">'1033' の値を返します。</span><span class="sxs-lookup"><span data-stu-id="7d27d-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="7d27d-124">'3082' の値を返します。</span><span class="sxs-lookup"><span data-stu-id="7d27d-124">Returns a value of '3082'.</span></span>
  

