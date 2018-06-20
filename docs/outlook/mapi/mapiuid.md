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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801540"
---
# <a name="mapiuid"></a><span data-ttu-id="13f2b-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="13f2b-103">MAPIUID</span></span>

  
  
<span data-ttu-id="13f2b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13f2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13f2b-105">サービス プロバイダーを一意に識別するために使用する[GUID](guid.md)構造体のバイト順の独立したバージョンです。</span><span class="sxs-lookup"><span data-stu-id="13f2b-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13f2b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="13f2b-106">Header file:</span></span>  <br/> |<span data-ttu-id="13f2b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13f2b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="13f2b-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="13f2b-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="13f2b-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="13f2b-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="13f2b-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="13f2b-110">Members</span></span>

 <span data-ttu-id="13f2b-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="13f2b-111">**ab**</span></span>
  
> <span data-ttu-id="13f2b-112">16 バイトの識別子を格納する配列。</span><span class="sxs-lookup"><span data-stu-id="13f2b-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13f2b-113">備考</span><span class="sxs-lookup"><span data-stu-id="13f2b-113">Remarks</span></span>

<span data-ttu-id="13f2b-114">**MAPIUID**構造体は、Intel® プロセッサのバイト順に格納する**GUID**構造体です。</span><span class="sxs-lookup"><span data-stu-id="13f2b-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="13f2b-115">MAPI では、同じ識別子を持つ 2 つの異なる項目の非常にまれな方法で**MAPIUID**の構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="13f2b-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="13f2b-116">**MAPIUID**構造体は、バイナリ プロパティ、または、バイトの順序を保存するか、または情報にアクセスするコンピューターに関係なく、ファイルとして保存できます。</span><span class="sxs-lookup"><span data-stu-id="13f2b-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="13f2b-117">**MAPIUID**構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="13f2b-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="13f2b-118">プロファイル セクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="13f2b-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="13f2b-119">エントリには、メッセージの識別子は、格納し、担当のサービス プロバイダーを識別するオブジェクトをブックに対応します。</span><span class="sxs-lookup"><span data-stu-id="13f2b-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="13f2b-120">メッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="13f2b-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="13f2b-121">検索キーの**MAPIUID**の識別子を生成するには、サービス プロバイダーは、 [IMAPISupport::NewUID](imapisupport-newuid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13f2b-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="13f2b-122">クライアントは、ネットワーク経由でメッセージを送信、ときに、プロトコルや送信の形式で、 **MAPIUID**のデータのバイト順を変更することはないを使用してください。</span><span class="sxs-lookup"><span data-stu-id="13f2b-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="13f2b-123">**MAPIUID**構造体を使用する方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="13f2b-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="13f2b-124">サービス プロバイダーの一意の識別子を登録します。</span><span class="sxs-lookup"><span data-stu-id="13f2b-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="13f2b-125">トランスポート オーダを設定</span><span class="sxs-lookup"><span data-stu-id="13f2b-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="13f2b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="13f2b-126">See also</span></span>



[<span data-ttu-id="13f2b-127">GUID</span><span class="sxs-lookup"><span data-stu-id="13f2b-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="13f2b-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="13f2b-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="13f2b-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="13f2b-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="13f2b-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="13f2b-130">MAPI Structures</span></span>](mapi-structures.md)

