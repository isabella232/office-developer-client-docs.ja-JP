---
title: PidTagIpmSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ee2e9e7f73e03e0a201a5ff41ea6e37a78c668a1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569576"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="23745-103">PidTagIpmSentMailEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="23745-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="23745-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23745-105">標準的な個人間メッセージ (IPM) の [送信済みアイテム フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23745-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23745-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="23745-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23745-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="23745-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="23745-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="23745-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23745-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="23745-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="23745-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="23745-110">Data type:</span></span>  <br/> |<span data-ttu-id="23745-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="23745-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="23745-112">領域:</span><span class="sxs-lookup"><span data-stu-id="23745-112">Area:</span></span>  <br/> |<span data-ttu-id="23745-113">Folder</span><span class="sxs-lookup"><span data-stu-id="23745-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23745-114">注釈</span><span class="sxs-lookup"><span data-stu-id="23745-114">Remarks</span></span>

<span data-ttu-id="23745-115">、送信した個人間のメッセージは通常、送信済みアイテム フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="23745-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="23745-116">クライアントは、送信されたメッセージの**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定するのにはこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="23745-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23745-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23745-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="23745-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="23745-118">Header files</span></span>

<span data-ttu-id="23745-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23745-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="23745-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23745-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="23745-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23745-121">Mapitags.h</span></span>
  
> <span data-ttu-id="23745-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23745-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23745-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="23745-123">See also</span></span>



[<span data-ttu-id="23745-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23745-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23745-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23745-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23745-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="23745-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23745-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="23745-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

