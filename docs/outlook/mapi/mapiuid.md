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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587167"
---
# <a name="mapiuid"></a><span data-ttu-id="0641e-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0641e-103">MAPIUID</span></span>

  
  
<span data-ttu-id="0641e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0641e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0641e-105">サービス プロバイダーを一意に識別するために使用する[GUID](guid.md)構造体のバイト順の独立したバージョンです。</span><span class="sxs-lookup"><span data-stu-id="0641e-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0641e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0641e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0641e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0641e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0641e-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0641e-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="0641e-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="0641e-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="0641e-110">Members</span><span class="sxs-lookup"><span data-stu-id="0641e-110">Members</span></span>

 <span data-ttu-id="0641e-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="0641e-111">**ab**</span></span>
  
> <span data-ttu-id="0641e-112">16 バイトの識別子を格納する配列。</span><span class="sxs-lookup"><span data-stu-id="0641e-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0641e-113">注釈</span><span class="sxs-lookup"><span data-stu-id="0641e-113">Remarks</span></span>

<span data-ttu-id="0641e-114">**MAPIUID**構造体は、Intel® プロセッサのバイト順に格納する**GUID**構造体です。</span><span class="sxs-lookup"><span data-stu-id="0641e-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="0641e-115">MAPI では、同じ識別子を持つ 2 つの異なる項目の非常にまれな方法で**MAPIUID**の構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="0641e-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="0641e-116">**MAPIUID**構造体は、バイナリ プロパティ、または、バイトの順序を保存するか、または情報にアクセスするコンピューターに関係なく、ファイルとして保存できます。</span><span class="sxs-lookup"><span data-stu-id="0641e-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="0641e-117">**MAPIUID**構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0641e-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="0641e-118">プロファイル セクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="0641e-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="0641e-119">エントリには、メッセージの識別子は、格納し、担当のサービス プロバイダーを識別するオブジェクトをブックに対応します。</span><span class="sxs-lookup"><span data-stu-id="0641e-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="0641e-120">メッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="0641e-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="0641e-121">検索キーの**MAPIUID**の識別子を生成するには、サービス プロバイダーは、 [IMAPISupport::NewUID](imapisupport-newuid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0641e-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="0641e-122">クライアントは、ネットワーク経由でメッセージを送信、ときに、プロトコルや送信の形式で、 **MAPIUID**のデータのバイト順を変更することはないを使用してください。</span><span class="sxs-lookup"><span data-stu-id="0641e-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="0641e-123">**MAPIUID**構造体を使用する方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0641e-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="0641e-124">サービス プロバイダー一意識別子の登録</span><span class="sxs-lookup"><span data-stu-id="0641e-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="0641e-125">転送順序の設定</span><span class="sxs-lookup"><span data-stu-id="0641e-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="0641e-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="0641e-126">See also</span></span>



[<span data-ttu-id="0641e-127">GUID</span><span class="sxs-lookup"><span data-stu-id="0641e-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="0641e-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0641e-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="0641e-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="0641e-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="0641e-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0641e-130">MAPI Structures</span></span>](mapi-structures.md)

