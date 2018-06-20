---
title: PidTagExpiryTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4666a5837c9f9f2ceb209088929aa3d343eb02f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802751"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="98d9b-103">PidTagExpiryTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="98d9b-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="98d9b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98d9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98d9b-105">日付と時刻のメッセージング システムがメッセージの内容を無効にするとが含まれています。</span><span class="sxs-lookup"><span data-stu-id="98d9b-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98d9b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="98d9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98d9b-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="98d9b-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="98d9b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="98d9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98d9b-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="98d9b-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="98d9b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="98d9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="98d9b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="98d9b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="98d9b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="98d9b-112">Area:</span></span>  <br/> |<span data-ttu-id="98d9b-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="98d9b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98d9b-114">備考</span><span class="sxs-lookup"><span data-stu-id="98d9b-114">Remarks</span></span>

<span data-ttu-id="98d9b-115">処理でメッセージング システムに配信された個人間のメッセージを送信するこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="98d9b-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98d9b-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="98d9b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98d9b-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="98d9b-117">Protocol specifications</span></span>

<span data-ttu-id="98d9b-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98d9b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98d9b-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="98d9b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98d9b-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98d9b-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98d9b-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="98d9b-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98d9b-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="98d9b-122">Header files</span></span>

<span data-ttu-id="98d9b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98d9b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="98d9b-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="98d9b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="98d9b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98d9b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="98d9b-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98d9b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98d9b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="98d9b-127">See also</span></span>



[<span data-ttu-id="98d9b-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98d9b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98d9b-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98d9b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98d9b-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="98d9b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98d9b-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="98d9b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

