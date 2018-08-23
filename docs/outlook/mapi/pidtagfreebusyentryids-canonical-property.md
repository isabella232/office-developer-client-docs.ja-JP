---
title: PidTagFreeBusyEntryIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyEntryIds
api_type:
- HeaderDef
ms.assetid: 8bc40ebf-76f2-49dd-af4b-4095bc07c639
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 603adf8df0c00efc592572fd9a46434f42845011
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564739"
---
# <a name="pidtagfreebusyentryids-canonical-property"></a><span data-ttu-id="1945b-103">PidTagFreeBusyEntryIds 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1945b-103">PidTagFreeBusyEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="1945b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1945b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1945b-105">代理人の情報メッセージ、ログイン中のユーザーとの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、「空き時間情報データ」と同じフォルダーの空き時間メッセージの**エントリ Id**が含まれています</span><span class="sxs-lookup"><span data-stu-id="1945b-105">Contains the **EntryIDs** for the delegate information message, the free/busy message of the logged in user, and the folder whose **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) is equal to "FreeBusy Data."</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1945b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1945b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1945b-107">PR_FREEBUSY_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="1945b-107">PR_FREEBUSY_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="1945b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1945b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1945b-109">0x36E4</span><span class="sxs-lookup"><span data-stu-id="1945b-109">0x36E4</span></span>  <br/> |
|<span data-ttu-id="1945b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1945b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1945b-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="1945b-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="1945b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1945b-112">Area:</span></span>  <br/> |<span data-ttu-id="1945b-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="1945b-113">MAPI container</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1945b-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1945b-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1945b-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1945b-115">Protocol specifications</span></span>

<span data-ttu-id="1945b-116">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1945b-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1945b-117">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1945b-117">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1945b-118">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1945b-118">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1945b-119">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="1945b-119">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="1945b-120">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1945b-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1945b-121">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のアイテムとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="1945b-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="1945b-122">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1945b-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1945b-123">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1945b-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1945b-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1945b-124">Header files</span></span>

<span data-ttu-id="1945b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1945b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1945b-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1945b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1945b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1945b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1945b-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1945b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1945b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1945b-129">See also</span></span>



[<span data-ttu-id="1945b-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1945b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1945b-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1945b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1945b-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1945b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1945b-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1945b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

