---
title: PidTagDisplayNamePrefix 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayNamePrefix
api_type:
- HeaderDef
ms.assetid: 014ce1aa-30b9-4106-82a1-447c370853cf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f35ddc2ccec73e485322345fc3bd7d8c7428bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360796"
---
# <a name="pidtagdisplaynameprefix-canonical-property"></a><span data-ttu-id="9538e-103">PidTagDisplayNamePrefix 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9538e-103">PidTagDisplayNamePrefix Canonical Property</span></span>

  
  
<span data-ttu-id="9538e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9538e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9538e-105">メッセージユーザーの表示名の接頭辞 (「見落とし」、「mr」、「mr」など) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9538e-105">Contains the display name prefix (such as Miss, Mr., Mrs.) for the messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9538e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9538e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9538e-107">PR_DISPLAY_NAME_PREFIX、PR_DISPLAY_NAME_PREFIX_A、PR_DISPLAY_NAME_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="9538e-107">PR_DISPLAY_NAME_PREFIX, PR_DISPLAY_NAME_PREFIX_A, PR_DISPLAY_NAME_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="9538e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9538e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9538e-109">0x3a45</span><span class="sxs-lookup"><span data-stu-id="9538e-109">0x3A45</span></span>  <br/> |
|<span data-ttu-id="9538e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9538e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9538e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9538e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9538e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9538e-112">Area:</span></span>  <br/> |<span data-ttu-id="9538e-113">MAPI メールユーザー</span><span class="sxs-lookup"><span data-stu-id="9538e-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9538e-114">解説</span><span class="sxs-lookup"><span data-stu-id="9538e-114">Remarks</span></span>

<span data-ttu-id="9538e-115">これらのプロパティは、メッセージングユーザーに関する id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9538e-115">These properties provide identification and access information about a messaging user.</span></span> <span data-ttu-id="9538e-116">コンテンツは、メッセージングユーザーおよびメッセージングユーザーの組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9538e-116">The content is defined by the messaging user and the messaging user's organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9538e-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9538e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9538e-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9538e-118">Protocol specifications</span></span>

<span data-ttu-id="9538e-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9538e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9538e-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9538e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9538e-121">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9538e-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9538e-122">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9538e-122">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="9538e-123">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9538e-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9538e-124">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9538e-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9538e-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9538e-125">Header files</span></span>

<span data-ttu-id="9538e-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9538e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9538e-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9538e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9538e-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9538e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9538e-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9538e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9538e-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="9538e-130">See also</span></span>



[<span data-ttu-id="9538e-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9538e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9538e-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9538e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9538e-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9538e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9538e-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9538e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

