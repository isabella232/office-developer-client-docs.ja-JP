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
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802912"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="17755-103">PidTagIpmTaskEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="17755-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="17755-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17755-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17755-105">Outlook の仕事フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="17755-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17755-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="17755-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17755-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="17755-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="17755-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="17755-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17755-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="17755-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="17755-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="17755-110">Data type:</span></span>  <br/> |<span data-ttu-id="17755-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="17755-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="17755-112">領域:</span><span class="sxs-lookup"><span data-stu-id="17755-112">Area:</span></span>  <br/> |<span data-ttu-id="17755-113">Folder</span><span class="sxs-lookup"><span data-stu-id="17755-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17755-114">注釈</span><span class="sxs-lookup"><span data-stu-id="17755-114">Remarks</span></span>

<span data-ttu-id="17755-115">このプロパティは読み取りまたはプロパティは、Stream オブジェクトのプロトコルを使用して書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="17755-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="17755-116">読み取られ、受信トレイ フォルダーまたはルート フォルダーに書き込まれることです。</span><span class="sxs-lookup"><span data-stu-id="17755-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="17755-117">ストアをプライマリ メッセージング ユーザーのストアは、代理ユーザーの場合ルート フォルダーを使用する必要があります、実装では、[受信トレイ] フォルダーを使用しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="17755-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17755-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="17755-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17755-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="17755-119">Protocol specifications</span></span>

<span data-ttu-id="17755-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17755-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17755-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="17755-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17755-122">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17755-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17755-123">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="17755-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="17755-124">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17755-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17755-125">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="17755-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17755-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="17755-126">Header files</span></span>

<span data-ttu-id="17755-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17755-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="17755-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="17755-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="17755-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17755-129">Mapitags.h</span></span>
  
> <span data-ttu-id="17755-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="17755-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17755-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="17755-131">See also</span></span>



[<span data-ttu-id="17755-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="17755-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17755-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="17755-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17755-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="17755-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17755-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="17755-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

