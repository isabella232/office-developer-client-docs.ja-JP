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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319461"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="d107e-103">PidLidContacts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d107e-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="d107e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d107e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d107e-105">アイテムに関連付けられた連絡先の名前を含む。</span><span class="sxs-lookup"><span data-stu-id="d107e-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d107e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d107e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d107e-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="d107e-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="d107e-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="d107e-108">Property set:</span></span>  <br/> |<span data-ttu-id="d107e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d107e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d107e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d107e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d107e-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="d107e-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="d107e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d107e-112">Data type:</span></span>  <br/> |<span data-ttu-id="d107e-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d107e-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d107e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d107e-114">Area:</span></span>  <br/> |<span data-ttu-id="d107e-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="d107e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d107e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d107e-116">Remarks</span></span>

<span data-ttu-id="d107e-117">このプロパティには **、dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) プロパティの値で参照される各アドレス帳 **EntryID** の PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティが含まれる。 </span><span class="sxs-lookup"><span data-stu-id="d107e-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="d107e-118">**dispidContactLinkEntry で参照されていない名前が含まれる場合があります**。</span><span class="sxs-lookup"><span data-stu-id="d107e-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d107e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d107e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d107e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d107e-120">Protocol specifications</span></span>

<span data-ttu-id="d107e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107e-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="d107e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d107e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107e-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d107e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d107e-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107e-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107e-126">ジャーナルに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d107e-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="d107e-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107e-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107e-128">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d107e-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d107e-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d107e-129">Header files</span></span>

<span data-ttu-id="d107e-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d107e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d107e-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d107e-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d107e-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="d107e-132">See also</span></span>



[<span data-ttu-id="d107e-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d107e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d107e-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d107e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d107e-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d107e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d107e-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d107e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

