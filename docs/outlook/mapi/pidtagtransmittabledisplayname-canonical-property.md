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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96eaf6c3f9ddc9d4bf6bc16ddc28a6f38bc311f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803634"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="42197-103">PidTagTransmittableDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="42197-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="42197-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42197-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42197-105">セキュリティで保護されたフォームでは変更できませんが、受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42197-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42197-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="42197-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42197-107">PR_TRANSMITABLE_DISPLAY_NAME、PR_TRANSMITABLE_DISPLAY_NAME_A、PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="42197-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="42197-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="42197-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42197-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="42197-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="42197-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="42197-110">Data type:</span></span>  <br/> |<span data-ttu-id="42197-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="42197-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="42197-112">領域:</span><span class="sxs-lookup"><span data-stu-id="42197-112">Area:</span></span>  <br/> |<span data-ttu-id="42197-113">Address</span><span class="sxs-lookup"><span data-stu-id="42197-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42197-114">注釈</span><span class="sxs-lookup"><span data-stu-id="42197-114">Remarks</span></span>

<span data-ttu-id="42197-115">これらのプロパティは、すべてのアドレス帳プロバイダーによって実装される必要があります。</span><span class="sxs-lookup"><span data-stu-id="42197-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="42197-116">メッセージと一緒に送信される受信者の表示名のバージョンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42197-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="42197-117">これらのプロパティではほとんどのアドレス帳プロバイダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティと同じ値があります。</span><span class="sxs-lookup"><span data-stu-id="42197-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="42197-118">PT_ERROR および MAPI の変更に名前を引用符を追加することでの表示名を取得、セキュリティで保護された表示名を持っていないプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="42197-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="42197-119">クライアント アプリケーションでは、改変やエントリの「なりすまし」を防ぐためにこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="42197-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="42197-120">なりすましの例では、(どのような Guy) の John Doe として John Doe が送信します。</span><span class="sxs-lookup"><span data-stu-id="42197-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="42197-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="42197-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42197-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="42197-122">Protocol specifications</span></span>

<span data-ttu-id="42197-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42197-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42197-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="42197-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="42197-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42197-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42197-126">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="42197-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="42197-127">[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42197-127">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42197-128">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="42197-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="42197-129">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42197-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42197-130">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="42197-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="42197-131">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42197-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42197-132">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="42197-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42197-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="42197-133">Header files</span></span>

<span data-ttu-id="42197-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42197-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="42197-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="42197-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="42197-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="42197-136">Mapitags.h</span></span>
  
> <span data-ttu-id="42197-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42197-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42197-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="42197-138">See also</span></span>



[<span data-ttu-id="42197-139">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="42197-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42197-140">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="42197-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42197-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="42197-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42197-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="42197-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

