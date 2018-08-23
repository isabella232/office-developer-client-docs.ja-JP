---
title: PidLidContacts 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a097b8e8071c08b82a05f3c8e0b021db8ec5107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585396"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="c85c2-103">PidLidContacts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85c2-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="c85c2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c85c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c85c2-105">アイテムに関連付けられている連絡先の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c85c2-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c85c2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c85c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c85c2-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="c85c2-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="c85c2-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c85c2-108">Property set:</span></span>  <br/> |<span data-ttu-id="c85c2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c85c2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c85c2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c85c2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c85c2-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="c85c2-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="c85c2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c85c2-112">Data type:</span></span>  <br/> |<span data-ttu-id="c85c2-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c85c2-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c85c2-114">領域:</span><span class="sxs-lookup"><span data-stu-id="c85c2-114">Area:</span></span>  <br/> |<span data-ttu-id="c85c2-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="c85c2-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c85c2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c85c2-116">Remarks</span></span>

<span data-ttu-id="c85c2-117">このプロパティには、 **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) のプロパティの値で参照されている各アドレス帳**エントリ Id**の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c85c2-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="c85c2-118">**DispidContactLinkEntry**で参照されていない名前の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c85c2-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c85c2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c85c2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c85c2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c85c2-120">Protocol specifications</span></span>

<span data-ttu-id="c85c2-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85c2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85c2-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c85c2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c85c2-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85c2-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85c2-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c85c2-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c85c2-125">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85c2-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85c2-126">プロパティとは、仕訳帳の許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c85c2-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="c85c2-127">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85c2-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85c2-128">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="c85c2-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c85c2-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c85c2-129">Header files</span></span>

<span data-ttu-id="c85c2-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c85c2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c85c2-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c85c2-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c85c2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c85c2-132">See also</span></span>



[<span data-ttu-id="c85c2-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85c2-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c85c2-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85c2-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c85c2-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c85c2-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c85c2-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c85c2-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

