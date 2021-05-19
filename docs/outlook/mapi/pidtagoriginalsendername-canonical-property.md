---
title: PidTagOriginalSenderName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 521fb544152dcb903450ff7dbd05ecbac808afe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342610"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="412ed-103">PidTagOriginalSenderName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="412ed-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="412ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="412ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="412ed-105">メッセージの最初のバージョンの送信者の表示名、つまり転送または返信前のメッセージが含まれる。</span><span class="sxs-lookup"><span data-stu-id="412ed-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="412ed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="412ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="412ed-107">PR_ORIGINAL_SENDER_NAME、PR_ORIGINAL_SENDER_NAME_A、PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="412ed-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="412ed-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="412ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="412ed-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="412ed-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="412ed-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="412ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="412ed-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="412ed-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="412ed-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="412ed-112">Area:</span></span>  <br/> |<span data-ttu-id="412ed-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="412ed-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="412ed-114">注釈</span><span class="sxs-lookup"><span data-stu-id="412ed-114">Remarks</span></span>

<span data-ttu-id="412ed-115">これらのプロパティは、メッセージの元の送信者のアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="412ed-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="412ed-116">メッセージの最初の送信時に、クライアント アプリケーションは、これらのプロパティを PR_SENDER_NAME ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティ **の値** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="412ed-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="412ed-117">メッセージが転送または返信された場合は、変更されません。</span><span class="sxs-lookup"><span data-stu-id="412ed-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="412ed-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="412ed-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="412ed-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="412ed-119">Protocol specifications</span></span>

<span data-ttu-id="412ed-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="412ed-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="412ed-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="412ed-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="412ed-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="412ed-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="412ed-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="412ed-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="412ed-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="412ed-124">Header files</span></span>

<span data-ttu-id="412ed-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="412ed-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="412ed-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="412ed-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="412ed-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="412ed-127">Mapitags.h</span></span>
  
> <span data-ttu-id="412ed-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="412ed-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="412ed-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="412ed-129">See also</span></span>



[<span data-ttu-id="412ed-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="412ed-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="412ed-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="412ed-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="412ed-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="412ed-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="412ed-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="412ed-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

