---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434831"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="ccf7e-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="ccf7e-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="ccf7e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccf7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccf7e-105">名前付きプロパティを記述し、それらの割り当てを検証する構造体の配列を検証します。</span><span class="sxs-lookup"><span data-stu-id="ccf7e-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccf7e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ccf7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="ccf7e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ccf7e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ccf7e-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ccf7e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ccf7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ccf7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ccf7e-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ccf7e-110">Called by:</span></span>  <br/> |<span data-ttu-id="ccf7e-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ccf7e-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="ccf7e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ccf7e-112">Parameters</span></span>

 <span data-ttu-id="ccf7e-113">_lppnameid_</span><span class="sxs-lookup"><span data-stu-id="ccf7e-113">_lppNameId_</span></span>
  
> <span data-ttu-id="ccf7e-114">順番名前付きプロパティを説明する[mapinameid](mapinameid.md)構造の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ccf7e-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="ccf7e-115">_cname_</span><span class="sxs-lookup"><span data-stu-id="ccf7e-115">_cNames_</span></span>
  
> <span data-ttu-id="ccf7e-116">順番_lppnameid_パラメーターで指定された、配列内の名前付きプロパティ構造体の数。</span><span class="sxs-lookup"><span data-stu-id="ccf7e-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ccf7e-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="ccf7e-117">Return value</span></span>

<span data-ttu-id="ccf7e-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="ccf7e-118">TRUE</span></span> 
  
> <span data-ttu-id="ccf7e-119">指定された1つ以上のプロパティ名の構造が無効です。</span><span class="sxs-lookup"><span data-stu-id="ccf7e-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="ccf7e-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="ccf7e-120">FALSE</span></span> 
  
> <span data-ttu-id="ccf7e-121">指定したプロパティ名の構造体はすべて有効です。</span><span class="sxs-lookup"><span data-stu-id="ccf7e-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccf7e-122">注釈</span><span class="sxs-lookup"><span data-stu-id="ccf7e-122">Remarks</span></span>

<span data-ttu-id="ccf7e-123">**fbadrglpnameid**関数は、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)または[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)の呼び出しを設定するときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="ccf7e-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

