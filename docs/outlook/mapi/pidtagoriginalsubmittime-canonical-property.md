---
title: PidTagOriginalSubmitTime の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 43d0387f1c25c5ac86168caaddddd9fb9171c827
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803100"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="d57f2-103">PidTagOriginalSubmitTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="d57f2-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="d57f2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d57f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d57f2-105">元の提出日と、レポート内のメッセージの時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d57f2-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d57f2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="d57f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d57f2-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="d57f2-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="d57f2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d57f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d57f2-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="d57f2-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="d57f2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="d57f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="d57f2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d57f2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d57f2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d57f2-112">Area:</span></span>  <br/> |<span data-ttu-id="d57f2-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="d57f2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d57f2-114">備考</span><span class="sxs-lookup"><span data-stu-id="d57f2-114">Remarks</span></span>

<span data-ttu-id="d57f2-115">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d57f2-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="d57f2-116">メッセージが転送された場合は変更されません。</span><span class="sxs-lookup"><span data-stu-id="d57f2-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="d57f2-117">レポートのみで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d57f2-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d57f2-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d57f2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d57f2-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d57f2-119">Protocol specifications</span></span>

<span data-ttu-id="d57f2-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57f2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57f2-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d57f2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d57f2-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57f2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57f2-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d57f2-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d57f2-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d57f2-124">Header files</span></span>

<span data-ttu-id="d57f2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d57f2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d57f2-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d57f2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d57f2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d57f2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d57f2-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d57f2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d57f2-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="d57f2-129">See also</span></span>



[<span data-ttu-id="d57f2-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d57f2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d57f2-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d57f2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d57f2-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="d57f2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d57f2-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="d57f2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

