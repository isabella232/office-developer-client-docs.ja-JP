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
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331858"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="313aa-103">PidTagTransmittableDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="313aa-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="313aa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="313aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="313aa-105">セキュリティで保護された形式の受信者の表示名が含まれており、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="313aa-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="313aa-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="313aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="313aa-107">PR_TRANSMITABLE_DISPLAY_NAME、PR_TRANSMITABLE_DISPLAY_NAME_A、PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="313aa-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="313aa-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="313aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="313aa-109">0x3a20</span><span class="sxs-lookup"><span data-stu-id="313aa-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="313aa-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="313aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="313aa-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="313aa-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="313aa-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="313aa-112">Area:</span></span>  <br/> |<span data-ttu-id="313aa-113">Address</span><span class="sxs-lookup"><span data-stu-id="313aa-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="313aa-114">解説</span><span class="sxs-lookup"><span data-stu-id="313aa-114">Remarks</span></span>

<span data-ttu-id="313aa-115">これらのプロパティは、すべてのアドレス帳プロバイダーで実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="313aa-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="313aa-116">これには、メッセージと共に送信される受信者の表示名のバージョンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="313aa-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="313aa-117">ほとんどのアドレス帳プロバイダーでは、これらのプロパティは**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと同じ値になります。</span><span class="sxs-lookup"><span data-stu-id="313aa-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="313aa-118">セキュリティで保護された表示名のないプロバイダーは、PT_ERROR と MAPI の名前を引用符で囲んで、表示名を変更します。</span><span class="sxs-lookup"><span data-stu-id="313aa-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="313aa-119">クライアントアプリケーションは、このプロパティを使用して、エントリの改ざんまたは "スプーフィング" を防止できます。</span><span class="sxs-lookup"><span data-stu-id="313aa-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="313aa-120">スプーフィングの例として、john doe を john (男の人) doe として送信することが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="313aa-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="313aa-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="313aa-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="313aa-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="313aa-122">Protocol specifications</span></span>

<span data-ttu-id="313aa-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313aa-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313aa-124">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="313aa-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="313aa-125">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313aa-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313aa-126">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="313aa-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="313aa-127">[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313aa-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313aa-128">ネームサービスプロバイダインターフェイス (NSPI) サーバーとのクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="313aa-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="313aa-129">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313aa-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313aa-130">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="313aa-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="313aa-131">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313aa-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313aa-132">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="313aa-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="313aa-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="313aa-133">Header files</span></span>

<span data-ttu-id="313aa-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="313aa-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="313aa-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="313aa-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="313aa-136">Mapitags</span><span class="sxs-lookup"><span data-stu-id="313aa-136">Mapitags.h</span></span>
  
> <span data-ttu-id="313aa-137">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="313aa-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="313aa-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="313aa-138">See also</span></span>



[<span data-ttu-id="313aa-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="313aa-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="313aa-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="313aa-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="313aa-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="313aa-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="313aa-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="313aa-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

