---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436434"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="4cce9-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="4cce9-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="4cce9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cce9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cce9-105">2つのアドレス帳**エントリ id**を複数の Exchange プロファイルで安全に比較します。</span><span class="sxs-lookup"><span data-stu-id="4cce9-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="4cce9-106">この関数は、 [IAddrBook:: compareentryids](iaddrbook-compareentryids.md)の置換関数です。</span><span class="sxs-lookup"><span data-stu-id="4cce9-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cce9-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4cce9-107">Header file:</span></span>  <br/> |<span data-ttu-id="4cce9-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="4cce9-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="4cce9-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="4cce9-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="4cce9-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="4cce9-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="4cce9-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4cce9-111">Called by:</span></span>  <br/> |<span data-ttu-id="4cce9-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4cce9-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="4cce9-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4cce9-113">Parameters</span></span>

 <span data-ttu-id="4cce9-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="4cce9-114">_pmsess_</span></span>
  
> <span data-ttu-id="4cce9-115">順番ログオンしている**imapisession**。</span><span class="sxs-lookup"><span data-stu-id="4cce9-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="4cce9-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4cce9-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4cce9-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="4cce9-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="4cce9-118">順番この関数がエントリ識別子の詳細を表示するために使用する exchange アドレス帳プロバイダーを含む exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce9-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="4cce9-119">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="4cce9-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="4cce9-120">このパラメーターが NULL またはゼロ MAPIUID の場合、この関数は[IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="4cce9-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="4cce9-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="4cce9-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="4cce9-122">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="4cce9-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="4cce9-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4cce9-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4cce9-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4cce9-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="4cce9-125">順番_lpEntryID1_パラメーターによって指定された最初のエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="4cce9-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="4cce9-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4cce9-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="4cce9-127">順番比較するアドレス帳のエントリを表す最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce9-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="4cce9-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4cce9-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="4cce9-129">順番_lpEntryID2_パラメーターによって指定された2番目のエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="4cce9-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="4cce9-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4cce9-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="4cce9-131">順番比較に使用されるアドレス帳のエントリを表す2番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce9-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="4cce9-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cce9-132">_ulFlags_</span></span>
  
> <span data-ttu-id="4cce9-133">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="4cce9-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4cce9-134">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="4cce9-134">_lpulResult_</span></span>
  
> <span data-ttu-id="4cce9-135">読み上げ比較結果が格納されている場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce9-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

