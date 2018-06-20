---
title: PidTagIpmTaskEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802912"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="b4fa0-103">PidTagIpmTaskEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b4fa0-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b4fa0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4fa0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4fa0-105">Outlook の仕事フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4fa0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4fa0-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b4fa0-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b4fa0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b4fa0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4fa0-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="b4fa0-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="b4fa0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4fa0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4fa0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4fa0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b4fa0-112">Area:</span></span>  <br/> |<span data-ttu-id="b4fa0-113">Folder</span><span class="sxs-lookup"><span data-stu-id="b4fa0-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4fa0-114">備考</span><span class="sxs-lookup"><span data-stu-id="b4fa0-114">Remarks</span></span>

<span data-ttu-id="b4fa0-115">このプロパティは読み取りまたはプロパティは、Stream オブジェクトのプロトコルを使用して書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="b4fa0-116">読み取られ、受信トレイ フォルダーまたはルート フォルダーに書き込まれることです。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="b4fa0-117">ストアをプライマリ メッセージング ユーザーのストアは、代理ユーザーの場合ルート フォルダーを使用する必要があります、実装では、[受信トレイ] フォルダーを使用しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4fa0-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b4fa0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4fa0-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b4fa0-119">Protocol specifications</span></span>

<span data-ttu-id="b4fa0-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4fa0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4fa0-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4fa0-122">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4fa0-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4fa0-123">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="b4fa0-124">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4fa0-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4fa0-125">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4fa0-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b4fa0-126">Header files</span></span>

<span data-ttu-id="b4fa0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4fa0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4fa0-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4fa0-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4fa0-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b4fa0-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4fa0-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4fa0-131">See also</span></span>



[<span data-ttu-id="b4fa0-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4fa0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4fa0-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4fa0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4fa0-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b4fa0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4fa0-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b4fa0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

