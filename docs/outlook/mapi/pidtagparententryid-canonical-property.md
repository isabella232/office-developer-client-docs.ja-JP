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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348231"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="935f7-103">PidTagParentEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="935f7-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="935f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="935f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="935f7-105">フォルダーまたはメッセージを含むフォルダーのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="935f7-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="935f7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="935f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="935f7-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="935f7-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="935f7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="935f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="935f7-109">0x0e09</span><span class="sxs-lookup"><span data-stu-id="935f7-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="935f7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="935f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="935f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="935f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="935f7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="935f7-112">Area:</span></span>  <br/> |<span data-ttu-id="935f7-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="935f7-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="935f7-114">解説</span><span class="sxs-lookup"><span data-stu-id="935f7-114">Remarks</span></span>

<span data-ttu-id="935f7-115">このプロパティは、すべてのフォルダーとメッセージのメッセージストアによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="935f7-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="935f7-116">メッセージストアのルートフォルダーの場合、このプロパティにはフォルダーの独自のエントリ識別子が格納されます。</span><span class="sxs-lookup"><span data-stu-id="935f7-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="935f7-117">**PR_PARENT_DISPLAY**([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) およびこのプロパティは相互に関連していません。</span><span class="sxs-lookup"><span data-stu-id="935f7-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="935f7-118">これらは完全に異なるコンテキストに属します。</span><span class="sxs-lookup"><span data-stu-id="935f7-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="935f7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="935f7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="935f7-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="935f7-120">Protocol specifications</span></span>

<span data-ttu-id="935f7-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="935f7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="935f7-123">[[OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-124">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="935f7-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="935f7-125">[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-126">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="935f7-126">Handles folder operations.</span></span>
    
<span data-ttu-id="935f7-127">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-128">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="935f7-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="935f7-129">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-130">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="935f7-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="935f7-131">[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-132">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="935f7-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="935f7-133">[[OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="935f7-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="935f7-134">オフラインアドレス帳 (OAB) のデータをサーバーからクライアントに配信する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="935f7-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="935f7-135">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="935f7-135">Header files</span></span>

<span data-ttu-id="935f7-136">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="935f7-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="935f7-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="935f7-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="935f7-138">Mapitags</span><span class="sxs-lookup"><span data-stu-id="935f7-138">Mapitags.h</span></span>
  
> <span data-ttu-id="935f7-139">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="935f7-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="935f7-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="935f7-140">See also</span></span>



[<span data-ttu-id="935f7-141">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="935f7-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="935f7-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="935f7-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="935f7-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="935f7-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="935f7-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="935f7-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="935f7-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="935f7-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

