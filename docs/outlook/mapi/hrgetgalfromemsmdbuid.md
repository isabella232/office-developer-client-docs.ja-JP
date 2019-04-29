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
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="598c6-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="598c6-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="598c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="598c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="598c6-105">_pEmsmdbUID_によって識別される Exchange サービスのグローバルアドレス帳のエントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="598c6-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="598c6-106">返されたエントリ id は、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="598c6-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="598c6-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="598c6-107">Header file:</span></span>  <br/> |<span data-ttu-id="598c6-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="598c6-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="598c6-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="598c6-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="598c6-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="598c6-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="598c6-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="598c6-111">Called by:</span></span>  <br/> |<span data-ttu-id="598c6-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="598c6-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="598c6-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="598c6-113">Parameters</span></span>

 <span data-ttu-id="598c6-114">_psess_</span><span class="sxs-lookup"><span data-stu-id="598c6-114">_pSess_</span></span>
  
> <span data-ttu-id="598c6-115">順番ログオンしている imapisession。</span><span class="sxs-lookup"><span data-stu-id="598c6-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="598c6-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="598c6-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="598c6-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="598c6-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="598c6-118">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="598c6-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="598c6-119">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="598c6-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="598c6-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="598c6-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="598c6-121">順番取得する Exchange サービスの GAL を識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="598c6-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="598c6-122">_pEmsmdbUID_が NULL またはゼロ UID の場合、この関数は、Exchange サービスの従来の GAL を取得します。</span><span class="sxs-lookup"><span data-stu-id="598c6-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="598c6-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="598c6-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="598c6-124">読み上げグローバルアドレス一覧のエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="598c6-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="598c6-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="598c6-125">_lppeid_</span></span>
  
> <span data-ttu-id="598c6-126">読み上げグローバルアドレス一覧のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="598c6-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="598c6-127">これは、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="598c6-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

