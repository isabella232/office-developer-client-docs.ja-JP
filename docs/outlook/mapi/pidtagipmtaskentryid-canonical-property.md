---
title: PidTagIpmTaskEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400251"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="281db-103">PidTagIpmTaskEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="281db-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="281db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="281db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="281db-105">Outlook の仕事フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="281db-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="281db-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="281db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="281db-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="281db-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="281db-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="281db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="281db-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="281db-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="281db-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="281db-110">Data type:</span></span>  <br/> |<span data-ttu-id="281db-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="281db-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="281db-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="281db-112">Area:</span></span>  <br/> |<span data-ttu-id="281db-113">Folder</span><span class="sxs-lookup"><span data-stu-id="281db-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="281db-114">備考</span><span class="sxs-lookup"><span data-stu-id="281db-114">Remarks</span></span>

<span data-ttu-id="281db-115">このプロパティは読み取りまたはプロパティは、Stream オブジェクトのプロトコルを使用して書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="281db-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="281db-116">読み取られ、受信トレイ フォルダーまたはルート フォルダーに書き込まれることです。</span><span class="sxs-lookup"><span data-stu-id="281db-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="281db-117">ストアをプライマリ メッセージング ユーザーのストアは、代理ユーザーの場合ルート フォルダーを使用する必要があります、実装では、[受信トレイ] フォルダーを使用しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="281db-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="281db-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="281db-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="281db-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="281db-119">Protocol specifications</span></span>

<span data-ttu-id="281db-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281db-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="281db-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="281db-122">[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281db-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281db-123">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="281db-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="281db-124">[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281db-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281db-125">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="281db-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="281db-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="281db-126">Header files</span></span>

<span data-ttu-id="281db-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="281db-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="281db-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="281db-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="281db-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="281db-129">Mapitags.h</span></span>
  
> <span data-ttu-id="281db-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="281db-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="281db-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="281db-131">See also</span></span>



[<span data-ttu-id="281db-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="281db-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="281db-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="281db-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="281db-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="281db-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="281db-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="281db-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

