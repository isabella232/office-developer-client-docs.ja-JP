---
title: PidLidContacts の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6182c9dfc0c4de24bd587e626fe74d02ed23968b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801856"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="e684c-103">PidLidContacts の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e684c-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="e684c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e684c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e684c-105">アイテムに関連付けられている連絡先の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e684c-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e684c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e684c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e684c-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="e684c-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="e684c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e684c-108">Property set:</span></span>  <br/> |<span data-ttu-id="e684c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e684c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e684c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e684c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e684c-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="e684c-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="e684c-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e684c-112">Data type:</span></span>  <br/> |<span data-ttu-id="e684c-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e684c-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e684c-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e684c-114">Area:</span></span>  <br/> |<span data-ttu-id="e684c-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="e684c-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e684c-116">備考</span><span class="sxs-lookup"><span data-stu-id="e684c-116">Remarks</span></span>

<span data-ttu-id="e684c-117">このプロパティには、 **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) のプロパティの値で参照されている各アドレス帳**エントリ Id**の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e684c-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="e684c-118">**DispidContactLinkEntry**で参照されていない名前の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e684c-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e684c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e684c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e684c-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e684c-120">Protocol specifications</span></span>

<span data-ttu-id="e684c-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e684c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e684c-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e684c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e684c-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e684c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e684c-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e684c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e684c-125">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e684c-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e684c-126">プロパティとは、仕訳帳の許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e684c-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="e684c-127">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e684c-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e684c-128">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e684c-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e684c-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e684c-129">Header files</span></span>

<span data-ttu-id="e684c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e684c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e684c-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e684c-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e684c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e684c-132">See also</span></span>



[<span data-ttu-id="e684c-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e684c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e684c-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e684c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e684c-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e684c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e684c-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e684c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

