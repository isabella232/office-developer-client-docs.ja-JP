---
title: PidLidHomeAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHomeAddress
api_type:
- COM
ms.assetid: 5e9c4258-46de-476e-8a64-be9e35a23a8b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8facbb2d3b4e83afc5fb4944607956c289f0bccb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396233"
---
# <a name="pidlidhomeaddress-canonical-property"></a><span data-ttu-id="64ac1-103">PidLidHomeAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="64ac1-103">PidLidHomeAddress Canonical Property</span></span>

  
  
<span data-ttu-id="64ac1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64ac1-105">連絡先の自宅の住所の完全なアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="64ac1-105">Specifies the complete address of the contact's home address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64ac1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="64ac1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64ac1-107">dispidHomeAddress</span><span class="sxs-lookup"><span data-stu-id="64ac1-107">dispidHomeAddress</span></span>  <br/> |
|<span data-ttu-id="64ac1-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="64ac1-108">Property set:</span></span>  <br/> |<span data-ttu-id="64ac1-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="64ac1-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="64ac1-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="64ac1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64ac1-111">0x0000801A</span><span class="sxs-lookup"><span data-stu-id="64ac1-111">0x0000801A</span></span>  <br/> |
|<span data-ttu-id="64ac1-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="64ac1-112">Data type:</span></span>  <br/> |<span data-ttu-id="64ac1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64ac1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="64ac1-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="64ac1-114">Area:</span></span>  <br/> |<span data-ttu-id="64ac1-115">Contact</span><span class="sxs-lookup"><span data-stu-id="64ac1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64ac1-116">備考</span><span class="sxs-lookup"><span data-stu-id="64ac1-116">Remarks</span></span>

<span data-ttu-id="64ac1-117">このプロパティは、他の物理アドレスのプロパティの組み合わせをする必要があり、クライアントのロケールに基づきます。</span><span class="sxs-lookup"><span data-stu-id="64ac1-117">This property should be a combination of other physical address properties, and is based on client locale.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64ac1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="64ac1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64ac1-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="64ac1-119">Protocol specifications</span></span>

<span data-ttu-id="64ac1-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64ac1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64ac1-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="64ac1-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64ac1-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64ac1-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64ac1-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="64ac1-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64ac1-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="64ac1-124">Header files</span></span>

<span data-ttu-id="64ac1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64ac1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="64ac1-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="64ac1-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64ac1-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="64ac1-127">See also</span></span>



[<span data-ttu-id="64ac1-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="64ac1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64ac1-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="64ac1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64ac1-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="64ac1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64ac1-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="64ac1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

