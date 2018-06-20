---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800296"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="7e76a-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="7e76a-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="7e76a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e76a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e76a-105">_PEmsmdbUID_によって識別される Exchange サービスのグローバル アドレス帳のエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="7e76a-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="7e76a-106">返されるエントリの識別子は、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e76a-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e76a-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7e76a-107">Header file:</span></span>  <br/> |<span data-ttu-id="7e76a-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="7e76a-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="7e76a-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7e76a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e76a-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="7e76a-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="7e76a-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7e76a-111">Called by:</span></span>  <br/> |<span data-ttu-id="7e76a-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7e76a-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="7e76a-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="7e76a-113">Parameters</span></span>

 <span data-ttu-id="7e76a-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="7e76a-114">_pSess_</span></span>
  
> <span data-ttu-id="7e76a-115">[in]IMAPISession にログオンします。</span><span class="sxs-lookup"><span data-stu-id="7e76a-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="7e76a-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7e76a-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7e76a-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="7e76a-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="7e76a-118">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="7e76a-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="7e76a-119">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7e76a-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7e76a-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="7e76a-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="7e76a-121">[in]取得する Exchange サービスのグローバル アドレス一覧を識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e76a-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="7e76a-122">_PEmsmdbUID_が NULL または UID が 0 の場合は、この関数は、レガシ Exchange サービスのグローバル アドレス一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e76a-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="7e76a-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="7e76a-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="7e76a-124">[out]グローバル アドレス一覧のエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e76a-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="7e76a-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="7e76a-125">_lppeid_</span></span>
  
> <span data-ttu-id="7e76a-126">[out]グローバル アドレス一覧のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e76a-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="7e76a-127">これは、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e76a-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

