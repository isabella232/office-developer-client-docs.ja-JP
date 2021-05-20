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
# <a name="mapiuid"></a><span data-ttu-id="36592-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="36592-103">MAPIUID</span></span>

  
  
<span data-ttu-id="36592-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36592-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36592-105">サービス プロバイダーを一意に識別するために使用される [GUID](guid.md) 構造のバイトオーダー独立バージョン。</span><span class="sxs-lookup"><span data-stu-id="36592-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36592-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="36592-106">Header file:</span></span>  <br/> |<span data-ttu-id="36592-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36592-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="36592-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="36592-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="36592-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="36592-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="36592-110">Members</span><span class="sxs-lookup"><span data-stu-id="36592-110">Members</span></span>

 <span data-ttu-id="36592-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="36592-111">**ab**</span></span>
  
> <span data-ttu-id="36592-112">16 バイトの識別子を含む配列。</span><span class="sxs-lookup"><span data-stu-id="36592-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36592-113">注釈</span><span class="sxs-lookup"><span data-stu-id="36592-113">Remarks</span></span>

<span data-ttu-id="36592-114">**MAPIUID 構造は\*\*\*\*、Intel** のプロセッサ バイトオーダーに® GUID 構造です。</span><span class="sxs-lookup"><span data-stu-id="36592-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="36592-115">MAPI は **、2 つの** 異なるアイテムが同じ識別子を持つ非常にまれな方法で MAPIUID 構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="36592-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="36592-116">**MAPIUID** 構造体は、情報を格納またはアクセスするコンピューターのバイト順序に関係なく、バイナリ プロパティまたはファイルとして格納できます。</span><span class="sxs-lookup"><span data-stu-id="36592-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="36592-117">**MAPIUID** 構造が使用されます。</span><span class="sxs-lookup"><span data-stu-id="36592-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="36592-118">プロファイル セクションを識別します。</span><span class="sxs-lookup"><span data-stu-id="36592-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="36592-119">メッセージ ストアオブジェクトとアドレス帳オブジェクトのエントリ識別子で、責任あるサービス プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="36592-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="36592-120">メッセージの **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="36592-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="36592-121">検索キーの **MAPIUID 識別子** を生成するために、サービス プロバイダーは [IMAPISupport::NewUID を呼び出します](imapisupport-newuid.md)。</span><span class="sxs-lookup"><span data-stu-id="36592-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="36592-122">クライアントがネットワークを通してメッセージを送信する場合、MAPIUID データのバイトオーダーを変更しないプロトコルまたは送信形式 **を使用する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="36592-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="36592-123">**MAPIUID 構造体の使用方法の** 詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="36592-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="36592-124">サービス プロバイダーの一意の識別子の登録</span><span class="sxs-lookup"><span data-stu-id="36592-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="36592-125">トランスポートの順序の設定</span><span class="sxs-lookup"><span data-stu-id="36592-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="36592-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="36592-126">See also</span></span>



[<span data-ttu-id="36592-127">GUID</span><span class="sxs-lookup"><span data-stu-id="36592-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="36592-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="36592-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="36592-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="36592-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="36592-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="36592-130">MAPI Structures</span></span>](mapi-structures.md)

