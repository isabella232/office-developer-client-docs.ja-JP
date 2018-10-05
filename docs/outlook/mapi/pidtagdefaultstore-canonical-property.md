---
title: PidTagDefaultStore 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385166"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="66322-103">PidTagDefaultStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66322-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="66322-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66322-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66322-105">メッセージ ストアがメッセージ ストアのテーブルの既定のメッセージ ストアの場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="66322-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66322-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="66322-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66322-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="66322-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="66322-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="66322-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66322-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="66322-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="66322-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="66322-110">Data type:</span></span>  <br/> |<span data-ttu-id="66322-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="66322-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="66322-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="66322-112">Area:</span></span>  <br/> |<span data-ttu-id="66322-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="66322-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66322-114">備考</span><span class="sxs-lookup"><span data-stu-id="66322-114">Remarks</span></span>

<span data-ttu-id="66322-115">このプロパティは、メッセージ ストアのテーブルの列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="66322-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="66322-116">値は、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) に基づいています。</span><span class="sxs-lookup"><span data-stu-id="66322-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66322-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="66322-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66322-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="66322-118">Protocol specifications</span></span>

<span data-ttu-id="66322-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66322-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66322-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="66322-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66322-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="66322-121">Header files</span></span>

<span data-ttu-id="66322-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66322-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="66322-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="66322-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="66322-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66322-124">Mapitags.h</span></span>
  
> <span data-ttu-id="66322-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="66322-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66322-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="66322-126">See also</span></span>



[<span data-ttu-id="66322-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="66322-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66322-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="66322-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66322-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66322-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66322-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66322-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

