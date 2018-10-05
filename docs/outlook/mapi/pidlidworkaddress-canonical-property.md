---
title: PidLidWorkAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWorkAddress
api_type:
- COM
ms.assetid: fc3c0ab3-6920-4e82-bc69-6c083159628f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7d09de701b9b7ecf168a914e40d91f514fa636cd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394966"
---
# <a name="pidlidworkaddress-canonical-property"></a><span data-ttu-id="8e088-103">PidLidWorkAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e088-103">PidLidWorkAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8e088-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e088-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e088-105">作業を終えたら、連絡先のアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="8e088-105">Specifies the contact's complete work address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e088-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8e088-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e088-107">dispidWorkAddress</span><span class="sxs-lookup"><span data-stu-id="8e088-107">dispidWorkAddress</span></span>  <br/> |
|<span data-ttu-id="8e088-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8e088-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e088-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8e088-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8e088-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8e088-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e088-111">0x0000801B</span><span class="sxs-lookup"><span data-stu-id="8e088-111">0x0000801B</span></span>  <br/> |
|<span data-ttu-id="8e088-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8e088-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e088-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e088-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8e088-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="8e088-114">Area:</span></span>  <br/> |<span data-ttu-id="8e088-115">Contact</span><span class="sxs-lookup"><span data-stu-id="8e088-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e088-116">備考</span><span class="sxs-lookup"><span data-stu-id="8e088-116">Remarks</span></span>

<span data-ttu-id="8e088-117">このプロパティは、他の物理アドレスのプロパティの組み合わせをする必要があり、クライアントのロケールに基づきます。</span><span class="sxs-lookup"><span data-stu-id="8e088-117">This property should be a combination of other physical address properties, and is based on client locale.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e088-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e088-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e088-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8e088-119">Protocol specifications</span></span>

<span data-ttu-id="8e088-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e088-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e088-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e088-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e088-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e088-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e088-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e088-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e088-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8e088-124">Header files</span></span>

<span data-ttu-id="8e088-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e088-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e088-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e088-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e088-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e088-127">See also</span></span>



[<span data-ttu-id="8e088-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e088-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e088-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e088-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e088-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e088-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e088-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e088-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

