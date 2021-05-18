---
title: PidLidOtherAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOtherAddress
api_type:
- COM
ms.assetid: 2b8acb69-4c84-4075-8457-d7aadce26c73
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b05e83e48bf144ca317a64f90fb533f6d7d1c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359074"
---
# <a name="pidlidotheraddress-canonical-property"></a><span data-ttu-id="606b8-103">PidLidOtherAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="606b8-103">PidLidOtherAddress Canonical Property</span></span>

  
  
<span data-ttu-id="606b8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="606b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="606b8-105">連絡先の他のアドレスの完全なアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="606b8-105">Specifies the complete address of the contact's other address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="606b8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="606b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="606b8-107">dispidOtherAddress</span><span class="sxs-lookup"><span data-stu-id="606b8-107">dispidOtherAddress</span></span>  <br/> |
|<span data-ttu-id="606b8-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="606b8-108">Property set:</span></span>  <br/> |<span data-ttu-id="606b8-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="606b8-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="606b8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="606b8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="606b8-111">0x0000801C</span><span class="sxs-lookup"><span data-stu-id="606b8-111">0x0000801C</span></span>  <br/> |
|<span data-ttu-id="606b8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="606b8-112">Data type:</span></span>  <br/> |<span data-ttu-id="606b8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="606b8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="606b8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="606b8-114">Area:</span></span>  <br/> |<span data-ttu-id="606b8-115">Contact</span><span class="sxs-lookup"><span data-stu-id="606b8-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="606b8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="606b8-116">Remarks</span></span>

<span data-ttu-id="606b8-117">このプロパティは、他の物理アドレス プロパティの組み合わせで、クライアント ロケールに基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="606b8-117">This property should be a combination of other physical address properties, and is based on client locale.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="606b8-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="606b8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="606b8-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="606b8-119">Protocol specifications</span></span>

<span data-ttu-id="606b8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="606b8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="606b8-121">プロパティ セットの定義と、関連するプロトコル仕様Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="606b8-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="606b8-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="606b8-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="606b8-123">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="606b8-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="606b8-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="606b8-124">Header files</span></span>

<span data-ttu-id="606b8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="606b8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="606b8-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="606b8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="606b8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="606b8-127">See also</span></span>



[<span data-ttu-id="606b8-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="606b8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="606b8-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="606b8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="606b8-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="606b8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="606b8-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="606b8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

