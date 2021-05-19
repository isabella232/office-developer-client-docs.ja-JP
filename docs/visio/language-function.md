---
title: LANGUAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: 異なる言語表現間の比較操作を許可します。 インターネット エンジニアリング タスク フォース言語タグ (BCP 47) の値をロケール ID (LCID) 値に変換する場合に最適です。
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424754"
---
# <a name="language-function"></a><span data-ttu-id="ee393-104">LANGUAGE 関数</span><span class="sxs-lookup"><span data-stu-id="ee393-104">LANGUAGE Function</span></span>

<span data-ttu-id="ee393-105">異なる言語表現間の比較操作を許可します。</span><span class="sxs-lookup"><span data-stu-id="ee393-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="ee393-106">インターネット エンジニアリング タスク フォース言語タグ (BCP 47) の値をロケール ID (LCID) 値に変換する場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="ee393-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="ee393-107">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="ee393-107">Version Information</span></span>

<span data-ttu-id="ee393-108">追加バージョン: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="ee393-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ee393-109">構文</span><span class="sxs-lookup"><span data-stu-id="ee393-109">Syntax</span></span>

 <span data-ttu-id="ee393-110">**LANGUAGE** _(_ lcid_or_bcp47 )</span><span class="sxs-lookup"><span data-stu-id="ee393-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="ee393-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee393-111">Parameters</span></span>

|<span data-ttu-id="ee393-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="ee393-112">**Name**</span></span>|<span data-ttu-id="ee393-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ee393-113">**Required/Optional**</span></span>|<span data-ttu-id="ee393-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ee393-114">**Data Type**</span></span>|<span data-ttu-id="ee393-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ee393-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ee393-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="ee393-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="ee393-117">必須</span><span class="sxs-lookup"><span data-stu-id="ee393-117">Required</span></span>  <br/> |<span data-ttu-id="ee393-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ee393-118">**String**</span></span> <br/> |<span data-ttu-id="ee393-119">言語の LCID または BCP 47 の値。</span><span class="sxs-lookup"><span data-stu-id="ee393-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="ee393-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="ee393-120">Return value</span></span>

<span data-ttu-id="ee393-121">整数</span><span class="sxs-lookup"><span data-stu-id="ee393-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="ee393-122">例</span><span class="sxs-lookup"><span data-stu-id="ee393-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="ee393-123">'1033' の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ee393-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="ee393-124">'3082' の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ee393-124">Returns a value of '3082'.</span></span>
  

