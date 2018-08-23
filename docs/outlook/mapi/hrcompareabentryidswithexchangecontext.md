---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eb91f4998f94ffafbc33b6024228945f7c91cf43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564991"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="15258-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="15258-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="15258-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15258-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15258-105">複数の Exchange プロファイルに安全に 2 つのアドレス帳**エントリ Id**を比較します。</span><span class="sxs-lookup"><span data-stu-id="15258-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="15258-106">[IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md)の交換用の関数です。</span><span class="sxs-lookup"><span data-stu-id="15258-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15258-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="15258-107">Header file:</span></span>  <br/> |<span data-ttu-id="15258-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="15258-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="15258-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="15258-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="15258-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="15258-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="15258-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="15258-111">Called by:</span></span>  <br/> |<span data-ttu-id="15258-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="15258-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="15258-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15258-113">Parameters</span></span>

 <span data-ttu-id="15258-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="15258-114">_pmsess_</span></span>
  
> <span data-ttu-id="15258-115">[in]**IMAPISession**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="15258-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="15258-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="15258-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="15258-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="15258-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="15258-118">[in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="15258-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="15258-119">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="15258-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="15258-120">このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="15258-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="15258-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="15258-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="15258-122">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="15258-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="15258-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="15258-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="15258-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="15258-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="15258-125">[in]_LpEntryID1_パラメーターで指定された最初のエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="15258-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="15258-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="15258-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="15258-127">[in]比較するアドレス帳のエントリを表す最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="15258-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="15258-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="15258-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="15258-129">[in]_LpEntryID2_パラメーターで指定された 2 番目のエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="15258-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="15258-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="15258-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="15258-131">[in]比較で使用される 2 番目のエントリの識別子へのポインターを比較するアドレス帳のエントリを表します。</span><span class="sxs-lookup"><span data-stu-id="15258-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="15258-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15258-132">_ulFlags_</span></span>
  
> <span data-ttu-id="15258-133">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="15258-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="15258-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="15258-134">_lpulResult_</span></span>
  
> <span data-ttu-id="15258-135">[out]比較の結果を格納する場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="15258-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

