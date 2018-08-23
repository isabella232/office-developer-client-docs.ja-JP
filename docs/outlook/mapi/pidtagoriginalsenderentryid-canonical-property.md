---
title: PidTagOriginalSenderEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f18587e28c6a3954b86dd58f0167e826d3086c51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803082"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="7fd12-103">PidTagOriginalSenderEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fd12-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7fd12-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7fd12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7fd12-105">最初のバージョンのメッセージを転送または返信する前にメッセージは、送信者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7fd12-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fd12-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7fd12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fd12-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7fd12-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7fd12-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7fd12-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7fd12-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="7fd12-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="7fd12-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7fd12-110">Data type:</span></span>  <br/> |<span data-ttu-id="7fd12-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7fd12-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7fd12-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7fd12-112">Area:</span></span>  <br/> |<span data-ttu-id="7fd12-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="7fd12-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fd12-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7fd12-114">Remarks</span></span>

<span data-ttu-id="7fd12-115">このプロパティは、メッセージの元の送信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="7fd12-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="7fd12-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fd12-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="7fd12-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7fd12-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7fd12-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7fd12-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fd12-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7fd12-119">Protocol specifications</span></span>

<span data-ttu-id="7fd12-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fd12-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fd12-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7fd12-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7fd12-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fd12-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fd12-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fd12-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fd12-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7fd12-124">Header files</span></span>

<span data-ttu-id="7fd12-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fd12-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fd12-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7fd12-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7fd12-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7fd12-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7fd12-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7fd12-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fd12-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fd12-129">See also</span></span>



[<span data-ttu-id="7fd12-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fd12-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fd12-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fd12-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fd12-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7fd12-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fd12-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7fd12-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

