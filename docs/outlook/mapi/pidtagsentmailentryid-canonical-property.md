---
title: PidTagSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342512"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="94da6-103">PidTagSentMailEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94da6-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="94da6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94da6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94da6-105">送信後にメッセージを移動するフォルダーのエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="94da6-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94da6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94da6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94da6-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="94da6-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="94da6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="94da6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94da6-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="94da6-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="94da6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94da6-110">Data type:</span></span>  <br/> |<span data-ttu-id="94da6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="94da6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="94da6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="94da6-112">Area:</span></span>  <br/> |<span data-ttu-id="94da6-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="94da6-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94da6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="94da6-114">Remarks</span></span>

<span data-ttu-id="94da6-115">このプロパティは、多くの場合、クライアント **アプリケーションの** 標準の送信アイテム フォルダーである PR_IPM_SENTMAIL_ENTRYID ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)プロパティからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="94da6-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="94da6-116">クライアント アプリケーションは、このプロパティを **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティと一緒に使用して、送信後のメッセージの処理を制御します。</span><span class="sxs-lookup"><span data-stu-id="94da6-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="94da6-117">どちらか一方を設定する必要がありますが、両方を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="94da6-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94da6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94da6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94da6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94da6-119">Protocol specifications</span></span>

<span data-ttu-id="94da6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94da6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94da6-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="94da6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94da6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94da6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94da6-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94da6-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="94da6-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94da6-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94da6-125">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="94da6-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94da6-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="94da6-126">Header files</span></span>

<span data-ttu-id="94da6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94da6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="94da6-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94da6-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="94da6-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94da6-129">Mapitags.h</span></span>
  
> <span data-ttu-id="94da6-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="94da6-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94da6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="94da6-131">See also</span></span>



[<span data-ttu-id="94da6-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="94da6-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94da6-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94da6-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94da6-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94da6-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94da6-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94da6-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

