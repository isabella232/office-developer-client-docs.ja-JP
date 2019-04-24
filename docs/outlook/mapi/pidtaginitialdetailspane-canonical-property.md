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
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346579"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="a8ffe-103">PidTagInitialDetailsPane 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8ffe-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="a8ffe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8ffe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8ffe-105">最初に表示する表示テンプレートのページを示します。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8ffe-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a8ffe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8ffe-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="a8ffe-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="a8ffe-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a8ffe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8ffe-109">0x3f08</span><span class="sxs-lookup"><span data-stu-id="a8ffe-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="a8ffe-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a8ffe-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8ffe-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a8ffe-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a8ffe-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a8ffe-112">Area:</span></span>  <br/> |<span data-ttu-id="a8ffe-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="a8ffe-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8ffe-114">解説</span><span class="sxs-lookup"><span data-stu-id="a8ffe-114">Remarks</span></span>

<span data-ttu-id="a8ffe-115">このプロパティは、ネームサービスプロバイダインターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクトに存在し、値がゼロ (0) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="a8ffe-116">オフラインアドレス帳内のオブジェクトに対して定義することはできません。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a8ffe-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a8ffe-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8ffe-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a8ffe-118">Protocol specifications</span></span>

<span data-ttu-id="a8ffe-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ffe-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ffe-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8ffe-121">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ffe-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ffe-122">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8ffe-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a8ffe-123">Header files</span></span>

<span data-ttu-id="a8ffe-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8ffe-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8ffe-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8ffe-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a8ffe-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a8ffe-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8ffe-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8ffe-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8ffe-128">See also</span></span>



[<span data-ttu-id="a8ffe-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a8ffe-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8ffe-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8ffe-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8ffe-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a8ffe-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8ffe-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a8ffe-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

