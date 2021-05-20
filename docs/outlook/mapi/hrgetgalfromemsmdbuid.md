---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439108"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="3c837-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="3c837-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="3c837-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c837-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c837-105">_pEmsmdbUID_ で識別される Exchangeアドレス帳のエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="3c837-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="3c837-106">返されるエントリ識別子は [、MAPIFreeBuffer を使用して解放する必要があります](mapifreebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="3c837-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c837-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3c837-107">Header file:</span></span>  <br/> |<span data-ttu-id="3c837-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="3c837-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="3c837-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="3c837-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c837-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="3c837-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="3c837-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3c837-111">Called by:</span></span>  <br/> |<span data-ttu-id="3c837-112">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3c837-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="3c837-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c837-113">Parameters</span></span>

 <span data-ttu-id="3c837-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="3c837-114">_pSess_</span></span>
  
> <span data-ttu-id="3c837-115">[in]ログオンしている IMAPISession。</span><span class="sxs-lookup"><span data-stu-id="3c837-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="3c837-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3c837-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="3c837-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="3c837-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="3c837-118">[in]エントリ識別子を開くのに使用するアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="3c837-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="3c837-119">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3c837-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="3c837-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="3c837-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="3c837-121">[in]取得するサービスの GAL を識別する **emsmdbUID** Exchangeポインター。</span><span class="sxs-lookup"><span data-stu-id="3c837-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="3c837-122">_pEmsmdbUID_ が NULL または 0 の UID の場合、この関数は、Exchange サービスの従来の GAL を取得します。</span><span class="sxs-lookup"><span data-stu-id="3c837-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="3c837-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="3c837-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="3c837-124">[out]グローバル アドレス一覧のエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3c837-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="3c837-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="3c837-125">_lppeid_</span></span>
  
> <span data-ttu-id="3c837-126">[out]グローバル アドレス一覧のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3c837-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="3c837-127">これは [MAPIFreeBuffer を使用して解放する必要があります](mapifreebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="3c837-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

