---
title: PidTagSearchFolderLastUsed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ff6df6eddc8e610341cb09ccb152f4ad748a984
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336534"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="b2181-103">PidTagSearchFolderLastUsed 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2181-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="b2181-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2181-105">フォルダーが最後にアクセスされた時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="b2181-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2181-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b2181-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2181-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="b2181-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="b2181-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b2181-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2181-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="b2181-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="b2181-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b2181-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2181-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b2181-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b2181-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b2181-112">Area:</span></span>  <br/> |<span data-ttu-id="b2181-113">検索</span><span class="sxs-lookup"><span data-stu-id="b2181-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2181-114">解説</span><span class="sxs-lookup"><span data-stu-id="b2181-114">Remarks</span></span>

<span data-ttu-id="b2181-115">このプロパティは、1601年1月1日の午前0時 (UTC) からの分数を分単位で書式設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2181-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2181-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b2181-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2181-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b2181-117">Protocol specifications</span></span>

<span data-ttu-id="b2181-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2181-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2181-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b2181-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2181-120">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2181-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2181-121">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2181-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2181-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b2181-122">Header files</span></span>

<span data-ttu-id="b2181-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2181-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2181-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b2181-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2181-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b2181-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b2181-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b2181-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2181-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2181-127">See also</span></span>



[<span data-ttu-id="b2181-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b2181-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2181-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2181-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2181-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b2181-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2181-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b2181-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

