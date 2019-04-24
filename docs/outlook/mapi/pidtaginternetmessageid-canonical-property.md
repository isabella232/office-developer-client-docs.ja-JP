---
title: PidTagInternetMessageId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358569"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="a6ef1-103">PidTagInternetMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6ef1-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="a6ef1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6ef1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6ef1-105">[RFC2822] で指定されているメッセージ ID フィールドに対応します。</span><span class="sxs-lookup"><span data-stu-id="a6ef1-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6ef1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a6ef1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6ef1-107">PR_INTERNET_MESSAGE_ID、PR_INTERNET_MESSAGE_ID_A、PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="a6ef1-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="a6ef1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a6ef1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6ef1-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="a6ef1-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="a6ef1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a6ef1-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6ef1-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6ef1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a6ef1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a6ef1-112">Area:</span></span>  <br/> |<span data-ttu-id="a6ef1-113">MIME</span><span class="sxs-lookup"><span data-stu-id="a6ef1-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6ef1-114">解説</span><span class="sxs-lookup"><span data-stu-id="a6ef1-114">Remarks</span></span>

<span data-ttu-id="a6ef1-115">これらのプロパティは、すべての電子メールメッセージに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ef1-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a6ef1-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a6ef1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6ef1-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a6ef1-117">Protocol specifications</span></span>

<span data-ttu-id="a6ef1-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6ef1-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6ef1-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6ef1-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6ef1-120">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6ef1-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6ef1-121">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6ef1-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6ef1-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a6ef1-122">Header files</span></span>

<span data-ttu-id="a6ef1-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6ef1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6ef1-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6ef1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6ef1-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a6ef1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a6ef1-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6ef1-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6ef1-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6ef1-127">See also</span></span>



[<span data-ttu-id="a6ef1-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a6ef1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6ef1-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6ef1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6ef1-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a6ef1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6ef1-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a6ef1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

