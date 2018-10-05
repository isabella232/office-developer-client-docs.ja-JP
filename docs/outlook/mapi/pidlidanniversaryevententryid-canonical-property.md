---
title: PidLidAnniversaryEventEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399628"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="29e63-103">PidLidAnniversaryEventEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="29e63-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="29e63-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29e63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29e63-105">予定、連絡先の記念日を表すエントリの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="29e63-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29e63-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="29e63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29e63-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="29e63-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="29e63-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="29e63-108">Property set:</span></span>  <br/> |<span data-ttu-id="29e63-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="29e63-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="29e63-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="29e63-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="29e63-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="29e63-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="29e63-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="29e63-112">Data type:</span></span>  <br/> |<span data-ttu-id="29e63-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="29e63-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="29e63-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="29e63-114">Area:</span></span>  <br/> |<span data-ttu-id="29e63-115">Contact</span><span class="sxs-lookup"><span data-stu-id="29e63-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29e63-116">備考</span><span class="sxs-lookup"><span data-stu-id="29e63-116">Remarks</span></span>

<span data-ttu-id="29e63-117">**DispidAnniversaryEventEID**プロパティで指定された予定は、 **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md))、 **dispidContactLinkSearchKey** ([を使用して、この連絡先にリンクする必要があります。PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md))、および**dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) のプロパティ] で詳細な[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)とします。</span><span class="sxs-lookup"><span data-stu-id="29e63-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="29e63-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="29e63-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29e63-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="29e63-119">Protocol specifications</span></span>

<span data-ttu-id="29e63-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29e63-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29e63-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="29e63-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29e63-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29e63-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29e63-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="29e63-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29e63-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="29e63-124">Header files</span></span>

<span data-ttu-id="29e63-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29e63-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="29e63-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="29e63-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29e63-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="29e63-127">See also</span></span>



[<span data-ttu-id="29e63-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="29e63-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29e63-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="29e63-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29e63-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="29e63-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29e63-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="29e63-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

