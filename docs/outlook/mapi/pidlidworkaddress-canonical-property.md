---
title: PidLidWorkAddress の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0ea3e2f88b3e0df2f358894cdf604dda651821b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802285"
---
# <a name="pidlidworkaddress-canonical-property"></a><span data-ttu-id="8dcea-103">PidLidWorkAddress の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8dcea-103">PidLidWorkAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8dcea-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8dcea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8dcea-105">作業を終えたら、連絡先のアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="8dcea-105">Specifies the contact's complete work address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8dcea-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8dcea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8dcea-107">dispidWorkAddress</span><span class="sxs-lookup"><span data-stu-id="8dcea-107">dispidWorkAddress</span></span>  <br/> |
|<span data-ttu-id="8dcea-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8dcea-108">Property set:</span></span>  <br/> |<span data-ttu-id="8dcea-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8dcea-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8dcea-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8dcea-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8dcea-111">0x0000801B</span><span class="sxs-lookup"><span data-stu-id="8dcea-111">0x0000801B</span></span>  <br/> |
|<span data-ttu-id="8dcea-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8dcea-112">Data type:</span></span>  <br/> |<span data-ttu-id="8dcea-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8dcea-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8dcea-114">領域:</span><span class="sxs-lookup"><span data-stu-id="8dcea-114">Area:</span></span>  <br/> |<span data-ttu-id="8dcea-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="8dcea-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dcea-116">備考</span><span class="sxs-lookup"><span data-stu-id="8dcea-116">Remarks</span></span>

<span data-ttu-id="8dcea-117">このプロパティは、他の物理アドレスのプロパティの組み合わせをする必要があり、クライアントのロケールに基づきます。</span><span class="sxs-lookup"><span data-stu-id="8dcea-117">This property should be a combination of other physical address properties, and is based on client locale.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8dcea-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8dcea-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8dcea-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8dcea-119">Protocol specifications</span></span>

<span data-ttu-id="8dcea-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dcea-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dcea-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8dcea-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8dcea-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dcea-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dcea-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8dcea-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8dcea-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8dcea-124">Header files</span></span>

<span data-ttu-id="8dcea-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8dcea-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8dcea-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8dcea-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8dcea-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8dcea-127">See also</span></span>



[<span data-ttu-id="8dcea-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8dcea-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8dcea-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8dcea-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8dcea-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8dcea-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8dcea-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8dcea-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

