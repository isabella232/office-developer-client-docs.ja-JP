---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432206"
---
# <a name="mapiuid"></a><span data-ttu-id="1a2a7-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1a2a7-103">MAPIUID</span></span>

  
  
<span data-ttu-id="1a2a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a2a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a2a7-105">サービスプロバイダーを一意に識別するために使用される[GUID](guid.md)構造のバイト順序に依存しないバージョン。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a2a7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1a2a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a2a7-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a2a7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1a2a7-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="1a2a7-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="1a2a7-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="1a2a7-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="1a2a7-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="1a2a7-110">Members</span></span>

 <span data-ttu-id="1a2a7-111">**l**</span><span class="sxs-lookup"><span data-stu-id="1a2a7-111">**ab**</span></span>
  
> <span data-ttu-id="1a2a7-112">16バイトの識別子を含む配列。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a2a7-113">注釈</span><span class="sxs-lookup"><span data-stu-id="1a2a7-113">Remarks</span></span>

<span data-ttu-id="1a2a7-114">**MAPIUID**構造体は、Intel ®プロセッサのバイト順に格納される**GUID**構造です。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="1a2a7-115">MAPI は、2つの異なるアイテムが同じ識別子を持つようにする方法で、 **MAPIUID**構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="1a2a7-116">**MAPIUID**構造体は、バイナリプロパティとして、または情報に格納またはアクセスするコンピューターのバイト順序に関係なく、ファイルとして保存できます。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="1a2a7-117">**MAPIUID**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="1a2a7-118">プロファイルセクションを識別する。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="1a2a7-119">メッセージストアとアドレス帳オブジェクトのエントリ識別子で、責任のあるサービスプロバイダを識別します。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="1a2a7-120">メッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="1a2a7-121">検索キーの**MAPIUID**識別子を生成するために、サービスプロバイダーは[imapisupport:: newuid](imapisupport-newuid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="1a2a7-122">クライアントがネットワーク経由でメッセージを送信する場合、 **MAPIUID**データのバイト順を変更しないプロトコルまたは転送形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="1a2a7-123">**MAPIUID**構造体の使用方法の詳細については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a2a7-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="1a2a7-124">サービスプロバイダーの一意識別子の登録</span><span class="sxs-lookup"><span data-stu-id="1a2a7-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="1a2a7-125">トランスポート順序の設定</span><span class="sxs-lookup"><span data-stu-id="1a2a7-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="1a2a7-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a2a7-126">See also</span></span>



[<span data-ttu-id="1a2a7-127">GUID</span><span class="sxs-lookup"><span data-stu-id="1a2a7-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="1a2a7-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1a2a7-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="1a2a7-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="1a2a7-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="1a2a7-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1a2a7-130">MAPI Structures</span></span>](mapi-structures.md)

