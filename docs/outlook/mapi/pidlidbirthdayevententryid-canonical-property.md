---
title: PidLidBirthdayEventEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 90d1dc8a9ce7f94238e8754cfbcaf88b702928f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342022"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="a67fc-103">PidLidBirthdayEventEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a67fc-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a67fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a67fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a67fc-105">連絡先の誕生日を表す、省略可能な予定の**EntryId**を指定します。</span><span class="sxs-lookup"><span data-stu-id="a67fc-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a67fc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a67fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a67fc-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="a67fc-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="a67fc-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a67fc-108">Property set:</span></span>  <br/> |<span data-ttu-id="a67fc-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a67fc-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a67fc-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a67fc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a67fc-111">0x0000804d</span><span class="sxs-lookup"><span data-stu-id="a67fc-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="a67fc-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a67fc-112">Data type:</span></span>  <br/> |<span data-ttu-id="a67fc-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a67fc-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a67fc-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a67fc-114">Area:</span></span>  <br/> |<span data-ttu-id="a67fc-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="a67fc-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a67fc-116">解説</span><span class="sxs-lookup"><span data-stu-id="a67fc-116">Remarks</span></span>

<span data-ttu-id="a67fc-117">このプロパティによって指定される予定は、 **dispidapptstateflags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md))、 **dispidapptstateflags** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md))**を使用して、この連絡先にリンクされている必要があります。** [[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で指定されているように、dispidcontactlinkname ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a67fc-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a67fc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a67fc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a67fc-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a67fc-119">Protocol specifications</span></span>

<span data-ttu-id="a67fc-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a67fc-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a67fc-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a67fc-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a67fc-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a67fc-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a67fc-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a67fc-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a67fc-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a67fc-124">Header files</span></span>

<span data-ttu-id="a67fc-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a67fc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a67fc-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a67fc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a67fc-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a67fc-127">See also</span></span>



[<span data-ttu-id="a67fc-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a67fc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a67fc-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a67fc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a67fc-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a67fc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a67fc-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a67fc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

