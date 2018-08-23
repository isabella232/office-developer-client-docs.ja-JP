---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b05baf1f819a821da3496cc63c2b2980894efd7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575715"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="dab7e-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="dab7e-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="dab7e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab7e-105">_PEmsmdbUID_によって識別される Exchange サービスのグローバル アドレス帳のエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="dab7e-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="dab7e-106">返されるエントリの識別子は、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dab7e-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dab7e-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dab7e-107">Header file:</span></span>  <br/> |<span data-ttu-id="dab7e-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="dab7e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="dab7e-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dab7e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="dab7e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="dab7e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="dab7e-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dab7e-111">Called by:</span></span>  <br/> |<span data-ttu-id="dab7e-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="dab7e-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="dab7e-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dab7e-113">Parameters</span></span>

 <span data-ttu-id="dab7e-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="dab7e-114">_pSess_</span></span>
  
> <span data-ttu-id="dab7e-115">[in]IMAPISession にログオンします。</span><span class="sxs-lookup"><span data-stu-id="dab7e-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="dab7e-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="dab7e-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dab7e-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="dab7e-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="dab7e-118">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="dab7e-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="dab7e-119">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="dab7e-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dab7e-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="dab7e-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="dab7e-121">[in]取得する Exchange サービスのグローバル アドレス一覧を識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dab7e-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="dab7e-122">_PEmsmdbUID_が NULL または UID が 0 の場合は、この関数は、レガシ Exchange サービスのグローバル アドレス一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="dab7e-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="dab7e-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="dab7e-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="dab7e-124">[out]グローバル アドレス一覧のエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dab7e-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="dab7e-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="dab7e-125">_lppeid_</span></span>
  
> <span data-ttu-id="dab7e-126">[out]グローバル アドレス一覧のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dab7e-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="dab7e-127">これは、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dab7e-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

