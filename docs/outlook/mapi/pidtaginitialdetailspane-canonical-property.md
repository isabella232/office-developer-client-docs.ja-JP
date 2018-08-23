---
title: PidTagInitialDetailsPane 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0ea7d0a17fdb6dba047cb97290d991ce384d4750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573937"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="f333a-103">PidTagInitialDetailsPane 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f333a-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="f333a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f333a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f333a-105">最初に表示する表示テンプレートのページを示します。</span><span class="sxs-lookup"><span data-stu-id="f333a-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f333a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f333a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f333a-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="f333a-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="f333a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f333a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f333a-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="f333a-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="f333a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f333a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f333a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f333a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f333a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f333a-112">Area:</span></span>  <br/> |<span data-ttu-id="f333a-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="f333a-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f333a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f333a-114">Remarks</span></span>

<span data-ttu-id="f333a-115">ネーム サービス プロバイダー インターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクト上に存在する必要があり、ゼロ (0) の値が必要です。</span><span class="sxs-lookup"><span data-stu-id="f333a-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="f333a-116">オフライン アドレス帳内のすべてのオブジェクトに対して定義されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="f333a-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f333a-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f333a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f333a-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f333a-118">Protocol specifications</span></span>

<span data-ttu-id="f333a-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f333a-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f333a-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f333a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f333a-121">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f333a-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f333a-122">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f333a-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f333a-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f333a-123">Header files</span></span>

<span data-ttu-id="f333a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f333a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f333a-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f333a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f333a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f333a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f333a-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f333a-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f333a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f333a-128">See also</span></span>



[<span data-ttu-id="f333a-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f333a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f333a-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f333a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f333a-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f333a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f333a-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f333a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

