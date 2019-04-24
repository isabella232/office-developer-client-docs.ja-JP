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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327850"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="c10f4-103">PidTagIpmTaskEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c10f4-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c10f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c10f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c10f4-105">Outlook のタスクフォルダーの**EntryID**を含みます。</span><span class="sxs-lookup"><span data-stu-id="c10f4-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c10f4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c10f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c10f4-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c10f4-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c10f4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c10f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c10f4-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="c10f4-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="c10f4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c10f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="c10f4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c10f4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c10f4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c10f4-112">Area:</span></span>  <br/> |<span data-ttu-id="c10f4-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="c10f4-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c10f4-114">解説</span><span class="sxs-lookup"><span data-stu-id="c10f4-114">Remarks</span></span>

<span data-ttu-id="c10f4-115">このプロパティは、property および Stream オブジェクトプロトコルを使用して、読み取りまたは書き込みができます。</span><span class="sxs-lookup"><span data-stu-id="c10f4-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="c10f4-116">これは、受信トレイまたはルートフォルダーに対して読み取りおよび書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="c10f4-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="c10f4-117">この実装では、ストアがプライマリメッセージングユーザーの場合は、受信トレイフォルダーを使用する必要があります。また、ストアが代理ユーザーの場合は、ルートフォルダーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c10f4-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c10f4-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c10f4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c10f4-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c10f4-119">Protocol specifications</span></span>

<span data-ttu-id="c10f4-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c10f4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c10f4-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c10f4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c10f4-122">[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c10f4-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c10f4-123">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c10f4-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="c10f4-124">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c10f4-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c10f4-125">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="c10f4-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c10f4-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c10f4-126">Header files</span></span>

<span data-ttu-id="c10f4-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c10f4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c10f4-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c10f4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c10f4-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c10f4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c10f4-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c10f4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c10f4-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c10f4-131">See also</span></span>



[<span data-ttu-id="c10f4-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c10f4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c10f4-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c10f4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c10f4-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c10f4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c10f4-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c10f4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

