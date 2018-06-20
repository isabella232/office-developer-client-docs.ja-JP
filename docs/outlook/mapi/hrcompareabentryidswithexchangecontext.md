---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 730c24a179cc6aaf8dc2068199ffc206d30156b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800275"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="bdb44-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="bdb44-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="bdb44-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bdb44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bdb44-105">複数の Exchange プロファイルに安全に 2 つのアドレス帳**エントリ Id**を比較します。</span><span class="sxs-lookup"><span data-stu-id="bdb44-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="bdb44-106">[IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md)の交換用の関数です。</span><span class="sxs-lookup"><span data-stu-id="bdb44-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bdb44-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bdb44-107">Header file:</span></span>  <br/> |<span data-ttu-id="bdb44-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="bdb44-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="bdb44-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="bdb44-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="bdb44-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="bdb44-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="bdb44-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bdb44-111">Called by:</span></span>  <br/> |<span data-ttu-id="bdb44-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bdb44-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="bdb44-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="bdb44-113">Parameters</span></span>

 <span data-ttu-id="bdb44-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="bdb44-114">_pmsess_</span></span>
  
> <span data-ttu-id="bdb44-115">[in]**IMAPISession**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="bdb44-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="bdb44-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bdb44-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bdb44-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="bdb44-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="bdb44-118">[in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bdb44-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="bdb44-119">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="bdb44-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="bdb44-120">このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="bdb44-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="bdb44-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="bdb44-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="bdb44-122">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="bdb44-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="bdb44-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bdb44-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bdb44-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="bdb44-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="bdb44-125">[in]_LpEntryID1_パラメーターで指定された最初のエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="bdb44-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="bdb44-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="bdb44-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="bdb44-127">[in]比較するアドレス帳のエントリを表す最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bdb44-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="bdb44-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="bdb44-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="bdb44-129">[in]_LpEntryID2_パラメーターで指定された 2 番目のエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="bdb44-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="bdb44-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="bdb44-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="bdb44-131">[in]比較で使用される 2 番目のエントリの識別子へのポインターを比較するアドレス帳のエントリを表します。</span><span class="sxs-lookup"><span data-stu-id="bdb44-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="bdb44-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bdb44-132">_ulFlags_</span></span>
  
> <span data-ttu-id="bdb44-133">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="bdb44-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="bdb44-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="bdb44-134">_lpulResult_</span></span>
  
> <span data-ttu-id="bdb44-135">[out]比較の結果を格納する場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bdb44-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

