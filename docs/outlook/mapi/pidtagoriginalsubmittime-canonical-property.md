---
title: PidTagOriginalSubmitTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341049"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="e0085-103">PidTagOriginalSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0085-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="e0085-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0085-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0085-105">レポート内のメッセージの元の提出日時を含む。</span><span class="sxs-lookup"><span data-stu-id="e0085-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0085-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e0085-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0085-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="e0085-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="e0085-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e0085-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0085-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="e0085-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="e0085-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e0085-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0085-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e0085-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e0085-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e0085-112">Area:</span></span>  <br/> |<span data-ttu-id="e0085-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="e0085-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0085-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e0085-114">Remarks</span></span>

<span data-ttu-id="e0085-115">メッセージの最初の送信時に、クライアント アプリケーションは、このプロパティを PR_CLIENT_SUBMIT_TIME **(** [PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0085-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="e0085-116">メッセージが転送された場合は変更されません。</span><span class="sxs-lookup"><span data-stu-id="e0085-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="e0085-117">これはレポートでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0085-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0085-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e0085-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0085-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e0085-119">Protocol specifications</span></span>

<span data-ttu-id="e0085-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0085-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0085-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e0085-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0085-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0085-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0085-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0085-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0085-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e0085-124">Header files</span></span>

<span data-ttu-id="e0085-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0085-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0085-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e0085-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0085-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0085-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e0085-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e0085-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0085-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0085-129">See also</span></span>



[<span data-ttu-id="e0085-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e0085-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0085-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0085-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0085-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e0085-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0085-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e0085-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

