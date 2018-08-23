---
title: PidTagOriginalSentRepresentingName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingName
api_type:
- COM
ms.assetid: 1be45cad-05a2-44cb-8c3d-7f6ac092fa0d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2d7261aadd304b731fbf0d88cbd93cbdc07c118
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587342"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="f5253-103">PidTagOriginalSentRepresentingName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5253-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="f5253-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5253-105">元のメッセージが送信されたメッセージのユーザーの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5253-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5253-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f5253-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5253-107">PR_ORIGINAL_SENT_REPRESENTING_NAME、PR_ORIGINAL_SENT_REPRESENTING_NAME_A、PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f5253-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f5253-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f5253-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5253-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="f5253-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="f5253-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f5253-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5253-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f5253-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f5253-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f5253-112">Area:</span></span>  <br/> |<span data-ttu-id="f5253-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="f5253-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5253-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f5253-114">Remarks</span></span>

<span data-ttu-id="f5253-115">表されるメッセージの差出人のアドレスのプロパティのこれらのプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="f5253-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="f5253-116">会話のスレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5253-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="f5253-117">別のクライアントの代わりにメッセージを送信するクライアント アプリケーションは、メッセージの最初の提出書類に**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) プロパティの値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5253-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="f5253-118">設定すると、そのことはありません変更してください。</span><span class="sxs-lookup"><span data-stu-id="f5253-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5253-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f5253-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5253-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f5253-120">Protocol specifications</span></span>

<span data-ttu-id="f5253-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5253-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5253-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f5253-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5253-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5253-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5253-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5253-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5253-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f5253-125">Header files</span></span>

<span data-ttu-id="f5253-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5253-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5253-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f5253-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5253-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5253-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f5253-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5253-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5253-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5253-130">See also</span></span>



[<span data-ttu-id="f5253-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5253-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5253-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5253-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5253-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f5253-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5253-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f5253-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

