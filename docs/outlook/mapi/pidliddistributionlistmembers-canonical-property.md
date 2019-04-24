---
title: PidLidDistributionListMembers 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335071"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="e930a-103">PidLidDistributionListMembers 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e930a-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="e930a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e930a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e930a-105">個人用配布リストのメンバーに対応するオブジェクトの entryids のリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="e930a-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e930a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e930a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e930a-107">dispiddlmembers</span><span class="sxs-lookup"><span data-stu-id="e930a-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="e930a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="e930a-108">Property set:</span></span>  <br/> |<span data-ttu-id="e930a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e930a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e930a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e930a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e930a-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="e930a-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="e930a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e930a-112">Data type:</span></span>  <br/> |<span data-ttu-id="e930a-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e930a-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e930a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e930a-114">Area:</span></span>  <br/> |<span data-ttu-id="e930a-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="e930a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e930a-116">解説</span><span class="sxs-lookup"><span data-stu-id="e930a-116">Remarks</span></span>

<span data-ttu-id="e930a-117">個人用配布リストのメンバーは、他の個人用配布リスト、連絡先に含まれている電子アドレス、グローバルアドレス一覧のユーザーまたは配布リスト、または1回限りの電子メールアドレスにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e930a-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="e930a-118">各 entryid の形式は、 [[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定された1回限りの entryid であるか、またはラップされた entryid である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e930a-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="e930a-119">このプロパティを設定する場合、クライアントまたはサーバーの合計サイズが15000バイト未満であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e930a-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="e930a-120">このプロパティは、個人用配布リストのメンバーに対応する1回限りの entryids のリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="e930a-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="e930a-121">これらの1回限りの entryids は、個人用配布リストのメンバーの表示名と電子メールアドレスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="e930a-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="e930a-122">クライアントまたはサーバーでこのプロパティが設定されている場合は、 **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) プロパティのエントリごとに、このプロパティ**dispiddlmembers**と同期する必要があります。**dispidDLOneOffMembers**内での同じ位置。</span><span class="sxs-lookup"><span data-stu-id="e930a-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e930a-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e930a-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e930a-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e930a-124">Protocol specifications</span></span>

<span data-ttu-id="e930a-125">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e930a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e930a-126">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e930a-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e930a-127">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e930a-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e930a-128">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e930a-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e930a-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e930a-129">Header files</span></span>

<span data-ttu-id="e930a-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e930a-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e930a-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e930a-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e930a-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e930a-132">See also</span></span>



[<span data-ttu-id="e930a-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e930a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e930a-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e930a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e930a-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e930a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e930a-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e930a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

