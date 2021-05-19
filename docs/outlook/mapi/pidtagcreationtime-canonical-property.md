---
title: PidTagCreationTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreationTime
api_type:
- HeaderDef
ms.assetid: 13122af2-06c8-4342-983d-e38178743d8f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de853c66f0ef4270f4c443881bfa163d4abfa3e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357898"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="e2640-103">PidTagCreationTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2640-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="e2640-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2640-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2640-105">メッセージの作成日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="e2640-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2640-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e2640-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2640-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="e2640-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="e2640-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e2640-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2640-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="e2640-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="e2640-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e2640-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2640-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e2640-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e2640-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e2640-112">Area:</span></span>  <br/> |<span data-ttu-id="e2640-113">メッセージ時刻</span><span class="sxs-lookup"><span data-stu-id="e2640-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2640-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e2640-114">Remarks</span></span>

<span data-ttu-id="e2640-115">メッセージ ストアは、作成するメッセージごとにこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2640-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2640-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e2640-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2640-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e2640-117">Protocol specifications</span></span>

<span data-ttu-id="e2640-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2640-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2640-119">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e2640-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e2640-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2640-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2640-121">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2640-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2640-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e2640-122">Header files</span></span>

<span data-ttu-id="e2640-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2640-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2640-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2640-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2640-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2640-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e2640-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e2640-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2640-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2640-127">See also</span></span>



[<span data-ttu-id="e2640-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e2640-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2640-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2640-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2640-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e2640-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2640-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e2640-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

