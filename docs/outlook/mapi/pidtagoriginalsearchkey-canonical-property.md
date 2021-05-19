---
title: PidTagOriginalSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d106a216e8d72c126f3293f9d492db73992c3872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355294"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="2ff27-103">PidTagOriginalSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ff27-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2ff27-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff27-105">アドレス帳から個人用アドレス帳または他の書き込み可能なアドレス帳にコピーされたエントリの元の検索キーを格納します。</span><span class="sxs-lookup"><span data-stu-id="2ff27-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ff27-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ff27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ff27-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2ff27-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2ff27-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2ff27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ff27-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="2ff27-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="2ff27-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2ff27-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ff27-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ff27-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ff27-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2ff27-112">Area:</span></span>  <br/> |<span data-ttu-id="2ff27-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="2ff27-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ff27-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2ff27-114">Remarks</span></span>

<span data-ttu-id="2ff27-115">このプロパティは、コピーされたエントリの元のソースに関する情報を含むプロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="2ff27-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="2ff27-116">未読レポートの場合、このプロパティには、レポートが生成される元のメッセージ受信者の検索キーのコピーが含まれる。</span><span class="sxs-lookup"><span data-stu-id="2ff27-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="2ff27-117">元の受信者が配布リストの一部である場合、配布リストの検索キーはレポートに対して保持されます。</span><span class="sxs-lookup"><span data-stu-id="2ff27-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ff27-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ff27-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ff27-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2ff27-119">Protocol specifications</span></span>

<span data-ttu-id="2ff27-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ff27-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ff27-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="2ff27-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ff27-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ff27-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ff27-123">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ff27-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ff27-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2ff27-124">Header files</span></span>

<span data-ttu-id="2ff27-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ff27-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ff27-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ff27-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ff27-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ff27-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2ff27-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2ff27-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ff27-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ff27-129">See also</span></span>



[<span data-ttu-id="2ff27-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2ff27-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ff27-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ff27-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ff27-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ff27-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ff27-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ff27-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

