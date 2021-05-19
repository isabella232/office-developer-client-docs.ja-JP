---
title: PidTagTransmittableDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331858"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="a52f1-103">PidTagTransmittableDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a52f1-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="a52f1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a52f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a52f1-105">変更できない安全なフォーム内の受信者の表示名を含む。</span><span class="sxs-lookup"><span data-stu-id="a52f1-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a52f1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a52f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a52f1-107">PR_TRANSMITABLE_DISPLAY_NAME、PR_TRANSMITABLE_DISPLAY_NAME_A、PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a52f1-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a52f1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a52f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a52f1-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="a52f1-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="a52f1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a52f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="a52f1-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a52f1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a52f1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a52f1-112">Area:</span></span>  <br/> |<span data-ttu-id="a52f1-113">Address</span><span class="sxs-lookup"><span data-stu-id="a52f1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a52f1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a52f1-114">Remarks</span></span>

<span data-ttu-id="a52f1-115">これらのプロパティは、すべてのアドレス帳プロバイダーによって実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a52f1-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="a52f1-116">メッセージと一緒に送信される受信者の表示名のバージョンが含まれる。</span><span class="sxs-lookup"><span data-stu-id="a52f1-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="a52f1-117">ほとんどのアドレス帳プロバイダーでは、これらのプロパティの値は、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="a52f1-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="a52f1-118">セキュリティで保護された表示名を持PT_ERRORプロバイダーは、名前の周囲に二重引用符を追加して表示名を変更します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="a52f1-119">クライアント アプリケーションは、このプロパティを使用して、エントリの変更や "スプーフィング" を防止できます。</span><span class="sxs-lookup"><span data-stu-id="a52f1-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="a52f1-120">スプーフィングの例は、John Doe を John (What a Guy) Doe として送信しています。</span><span class="sxs-lookup"><span data-stu-id="a52f1-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a52f1-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a52f1-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a52f1-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a52f1-122">Protocol specifications</span></span>

<span data-ttu-id="a52f1-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a52f1-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a52f1-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a52f1-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a52f1-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a52f1-126">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="a52f1-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a52f1-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a52f1-128">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとのクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="a52f1-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a52f1-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a52f1-130">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a52f1-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a52f1-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a52f1-132">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a52f1-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a52f1-133">Header files</span></span>

<span data-ttu-id="a52f1-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a52f1-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="a52f1-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a52f1-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="a52f1-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a52f1-136">Mapitags.h</span></span>
  
> <span data-ttu-id="a52f1-137">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a52f1-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a52f1-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a52f1-138">See also</span></span>



[<span data-ttu-id="a52f1-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a52f1-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a52f1-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a52f1-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a52f1-141">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a52f1-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a52f1-142">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a52f1-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

