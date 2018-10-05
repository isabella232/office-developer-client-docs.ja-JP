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
ms.openlocfilehash: 57b65f8423cbbc48e3eac066c45cab0fcc90fe18
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389016"
---
# <a name="pidtagfreebusyentryids-canonical-property"></a><span data-ttu-id="8c81e-103">PidTagFreeBusyEntryIds 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c81e-103">PidTagFreeBusyEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="8c81e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c81e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c81e-105">代理人の情報メッセージ、ログイン中のユーザーとの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、「空き時間情報データ」と同じフォルダーの空き時間メッセージの**エントリ Id**が含まれています</span><span class="sxs-lookup"><span data-stu-id="8c81e-105">Contains the **EntryIDs** for the delegate information message, the free/busy message of the logged in user, and the folder whose **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) is equal to "FreeBusy Data."</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c81e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8c81e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c81e-107">PR_FREEBUSY_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="8c81e-107">PR_FREEBUSY_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="8c81e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8c81e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c81e-109">0x36E4</span><span class="sxs-lookup"><span data-stu-id="8c81e-109">0x36E4</span></span>  <br/> |
|<span data-ttu-id="8c81e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8c81e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c81e-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8c81e-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8c81e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8c81e-112">Area:</span></span>  <br/> |<span data-ttu-id="8c81e-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="8c81e-113">MAPI container</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8c81e-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8c81e-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c81e-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8c81e-115">Protocol specifications</span></span>

<span data-ttu-id="8c81e-116">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c81e-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c81e-117">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c81e-117">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c81e-118">[[MS OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c81e-118">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c81e-119">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="8c81e-119">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="8c81e-120">[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c81e-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c81e-121">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のアイテムとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="8c81e-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8c81e-122">[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c81e-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c81e-123">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c81e-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c81e-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8c81e-124">Header files</span></span>

<span data-ttu-id="8c81e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c81e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c81e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c81e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c81e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c81e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8c81e-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c81e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c81e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c81e-129">See also</span></span>



[<span data-ttu-id="8c81e-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c81e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c81e-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c81e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c81e-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8c81e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c81e-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8c81e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

