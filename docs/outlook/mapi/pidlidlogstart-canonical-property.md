---
title: PidLidLogStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 55ba18a1dcbce5e3f7996184dae45a638f9531e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802034"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="b7436-103">PidLidLogStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7436-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="b7436-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7436-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7436-105">ジャーナル メッセージの開始日時を表します。</span><span class="sxs-lookup"><span data-stu-id="b7436-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7436-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b7436-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7436-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="b7436-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="b7436-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b7436-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7436-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="b7436-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="b7436-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b7436-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7436-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="b7436-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="b7436-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b7436-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7436-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b7436-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b7436-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b7436-114">Area:</span></span>  <br/> |<span data-ttu-id="b7436-115">ジャーナル</span><span class="sxs-lookup"><span data-stu-id="b7436-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7436-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b7436-116">Remarks</span></span>

<span data-ttu-id="b7436-117">時刻を世界協定時刻 (UTC) で活動を開始したときは、 **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) のプロパティと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7436-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7436-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7436-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7436-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7436-119">Protocol specifications</span></span>

<span data-ttu-id="b7436-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7436-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7436-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7436-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7436-122">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7436-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7436-123">プロパティとは、仕訳帳の許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7436-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7436-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7436-124">Header files</span></span>

<span data-ttu-id="b7436-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7436-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7436-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7436-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7436-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7436-127">See also</span></span>



[<span data-ttu-id="b7436-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7436-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7436-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7436-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7436-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7436-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7436-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7436-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

