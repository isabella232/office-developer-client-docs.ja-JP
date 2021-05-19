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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335071"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="92446-103">PidLidDistributionListMembers 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="92446-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="92446-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92446-105">個人用配布リストのメンバーに対応するオブジェクトの EntryIds の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="92446-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92446-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="92446-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92446-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="92446-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="92446-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="92446-108">Property set:</span></span>  <br/> |<span data-ttu-id="92446-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="92446-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="92446-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="92446-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="92446-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="92446-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="92446-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="92446-112">Data type:</span></span>  <br/> |<span data-ttu-id="92446-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="92446-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="92446-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="92446-114">Area:</span></span>  <br/> |<span data-ttu-id="92446-115">Contact</span><span class="sxs-lookup"><span data-stu-id="92446-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92446-116">注釈</span><span class="sxs-lookup"><span data-stu-id="92446-116">Remarks</span></span>

<span data-ttu-id="92446-117">個人用配布リストのメンバーには、他の個人用配布リスト、連絡先に含まれる電子アドレス、グローバル アドレス一覧のユーザーまたは配布リスト、または 1 回限定の電子メール アドレスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="92446-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="92446-118">各 EntryId の形式は [、[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) で指定されている 1 回限りの EntryId か、ラップされた EntryId のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="92446-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="92446-119">このプロパティを設定する場合、クライアントまたはサーバーは、その合計サイズが 15,000 バイト未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="92446-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="92446-120">このプロパティは、個人用配布リストのメンバーに対応する 1 回限定の EntryId の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="92446-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="92446-121">これらの 1 回限定の EntryIds は、個人用配布リスト メンバーの表示名と電子メール アドレスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="92446-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="92446-122">クライアントまたはサーバーでこのプロパティを設定する場合は **、dispidDLOneOffMembers** [(PidLidDistributionListOneOffMembers)](pidliddistributionlistoneoffmembers-canonical-property.md)プロパティ内の各エントリについて、このプロパティ **dispidDLOneOffMembers と同期する必要があります。dispidDLOneOffMembers** 内に同じ位置にエントリが必要です。 </span><span class="sxs-lookup"><span data-stu-id="92446-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92446-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="92446-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92446-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="92446-124">Protocol specifications</span></span>

<span data-ttu-id="92446-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92446-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92446-126">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="92446-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92446-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92446-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92446-128">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="92446-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92446-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="92446-129">Header files</span></span>

<span data-ttu-id="92446-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92446-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="92446-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="92446-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92446-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="92446-132">See also</span></span>



[<span data-ttu-id="92446-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="92446-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92446-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="92446-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92446-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="92446-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92446-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="92446-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

