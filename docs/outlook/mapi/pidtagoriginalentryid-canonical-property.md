---
title: PidTagOriginalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f3f4f42d91c4091943d6183508e2bc76c17197fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342722"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="a5f06-103">PidTagOriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5f06-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a5f06-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5f06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5f06-105">アドレス帳から個人用アドレス帳またはその他の書き込み可能なアドレス帳にコピーされたエントリの元のエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="a5f06-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5f06-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a5f06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5f06-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a5f06-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a5f06-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a5f06-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5f06-109">0x3a12</span><span class="sxs-lookup"><span data-stu-id="a5f06-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="a5f06-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a5f06-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5f06-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a5f06-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a5f06-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a5f06-112">Area:</span></span>  <br/> |<span data-ttu-id="a5f06-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="a5f06-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5f06-114">解説</span><span class="sxs-lookup"><span data-stu-id="a5f06-114">Remarks</span></span>

<span data-ttu-id="a5f06-115">このプロパティは、コピーされたエントリの元のソースに関する情報を含むプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="a5f06-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="a5f06-116">非開封レポートの場合、このプロパティには、レポートが生成される元のメッセージ受信者のエントリ id のコピーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a5f06-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="a5f06-117">元の受信者が配布リストの一部である場合は、配布リストのエントリ識別子がレポート用に保持されます。</span><span class="sxs-lookup"><span data-stu-id="a5f06-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5f06-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a5f06-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5f06-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a5f06-119">Protocol specifications</span></span>

<span data-ttu-id="a5f06-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5f06-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5f06-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5f06-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5f06-122">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5f06-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5f06-123">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5f06-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="a5f06-124">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5f06-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5f06-125">サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="a5f06-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5f06-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a5f06-126">Header files</span></span>

<span data-ttu-id="a5f06-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5f06-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5f06-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5f06-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5f06-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a5f06-129">Mapitags.h</span></span>
  
> <span data-ttu-id="a5f06-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a5f06-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5f06-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5f06-131">See also</span></span>



[<span data-ttu-id="a5f06-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a5f06-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5f06-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5f06-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5f06-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5f06-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5f06-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5f06-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

