---
title: PidTagParentEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401217"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="10adc-103">PidTagParentEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10adc-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="10adc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10adc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10adc-105">フォルダーまたはメッセージを含むフォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10adc-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10adc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="10adc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10adc-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="10adc-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="10adc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="10adc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10adc-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="10adc-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="10adc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="10adc-110">Data type:</span></span>  <br/> |<span data-ttu-id="10adc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="10adc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="10adc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="10adc-112">Area:</span></span>  <br/> |<span data-ttu-id="10adc-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="10adc-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10adc-114">備考</span><span class="sxs-lookup"><span data-stu-id="10adc-114">Remarks</span></span>

<span data-ttu-id="10adc-115">このプロパティは、すべてのフォルダーとメッセージのメッセージ ・ ストアによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="10adc-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="10adc-116">メッセージ ストアのルート フォルダーには、このプロパティには、フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10adc-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="10adc-117">**PR_PARENT_DISPLAY**([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) と、このプロパティは互いに関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="10adc-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="10adc-118">まったく異なるコンテキストに属しているとします。</span><span class="sxs-lookup"><span data-stu-id="10adc-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10adc-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="10adc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10adc-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="10adc-120">Protocol specifications</span></span>

<span data-ttu-id="10adc-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="10adc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10adc-123">[[MS OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-124">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="10adc-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="10adc-125">[[MS OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-126">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="10adc-126">Handles folder operations.</span></span>
    
<span data-ttu-id="10adc-127">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="10adc-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="10adc-129">[[MS OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-130">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="10adc-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="10adc-131">[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-132">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="10adc-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="10adc-133">[[MS OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10adc-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10adc-134">オフライン アドレス帳 (OAB) のデータをサーバーからクライアントに配信する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="10adc-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10adc-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="10adc-135">Header files</span></span>

<span data-ttu-id="10adc-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10adc-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="10adc-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="10adc-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="10adc-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10adc-138">Mapitags.h</span></span>
  
> <span data-ttu-id="10adc-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10adc-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10adc-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="10adc-140">See also</span></span>



[<span data-ttu-id="10adc-141">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10adc-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="10adc-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="10adc-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10adc-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="10adc-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10adc-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="10adc-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10adc-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="10adc-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

