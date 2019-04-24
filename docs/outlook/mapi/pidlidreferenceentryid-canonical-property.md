---
title: PidLidReferenceEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReferenceEntryId
api_type:
- COM
ms.assetid: 42e7c3ac-1a04-4e3f-bf99-ef3f8fc45892
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f5bad81f6317522430b92324ff497754376e0f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315926"
---
# <a name="pidlidreferenceentryid-canonical-property"></a><span data-ttu-id="a0dc1-103">PidLidReferenceEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0dc1-103">PidLidReferenceEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a0dc1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0dc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0dc1-105">連絡先の参照[エントリ id](entryid.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0dc1-105">Specifies the reference [ENTRYID](entryid.md) for the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0dc1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a0dc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0dc1-107">dispidReferenceEID</span><span class="sxs-lookup"><span data-stu-id="a0dc1-107">dispidReferenceEID</span></span>  <br/> |
|<span data-ttu-id="a0dc1-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a0dc1-108">Property set:</span></span>  <br/> |<span data-ttu-id="a0dc1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a0dc1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a0dc1-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a0dc1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a0dc1-111">0x000085bd</span><span class="sxs-lookup"><span data-stu-id="a0dc1-111">0x000085BD</span></span>  <br/> |
|<span data-ttu-id="a0dc1-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a0dc1-112">Data type:</span></span>  <br/> |<span data-ttu-id="a0dc1-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a0dc1-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a0dc1-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a0dc1-114">Area:</span></span>  <br/> |<span data-ttu-id="a0dc1-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="a0dc1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0dc1-116">解説</span><span class="sxs-lookup"><span data-stu-id="a0dc1-116">Remarks</span></span>

<span data-ttu-id="a0dc1-117">このプロパティが存在する場合、このプロパティは連絡先の**EntryId**の値と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a0dc1-117">If present, this property should be equal to the value of the **EntryId** of the contact.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a0dc1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a0dc1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0dc1-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a0dc1-119">Protocol specifications</span></span>

<span data-ttu-id="a0dc1-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dc1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0dc1-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0dc1-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0dc1-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dc1-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0dc1-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0dc1-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0dc1-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a0dc1-124">Header files</span></span>

<span data-ttu-id="a0dc1-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0dc1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0dc1-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0dc1-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0dc1-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0dc1-127">See also</span></span>



[<span data-ttu-id="a0dc1-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a0dc1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0dc1-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0dc1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0dc1-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a0dc1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0dc1-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a0dc1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

