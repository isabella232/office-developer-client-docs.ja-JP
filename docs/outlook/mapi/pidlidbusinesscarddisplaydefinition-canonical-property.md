---
title: PidLidBusinessCardDisplayDefinition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342036"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="91b85-103">PidLidBusinessCardDisplayDefinition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91b85-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="91b85-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91b85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91b85-105">連絡先を名刺として表示するためのユーザーカスタマイズの詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="91b85-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91b85-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91b85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91b85-107">dispidbcdisplaydefinition</span><span class="sxs-lookup"><span data-stu-id="91b85-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="91b85-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="91b85-108">Property set:</span></span>  <br/> |<span data-ttu-id="91b85-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="91b85-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="91b85-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="91b85-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91b85-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="91b85-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="91b85-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91b85-112">Data type:</span></span>  <br/> |<span data-ttu-id="91b85-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="91b85-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="91b85-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="91b85-114">Area:</span></span>  <br/> |<span data-ttu-id="91b85-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="91b85-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91b85-116">解説</span><span class="sxs-lookup"><span data-stu-id="91b85-116">Remarks</span></span>

<span data-ttu-id="91b85-117">名刺のレイアウトは、画像と複数のテキストフィールドとして表すことができます。</span><span class="sxs-lookup"><span data-stu-id="91b85-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="91b85-118">画像は、連絡先の写真、またはカードの画像のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="91b85-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="91b85-119">テキストフィールドは、連絡先の他のプロパティセットからの値と、ユーザーによって提供されるオプションのカスタマイズされたラベル文字列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="91b85-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="91b85-120">マルチバイト値は、バッファーにリトルエンディアン形式で格納されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="91b85-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91b85-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91b85-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91b85-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="91b85-122">Protocol specifications</span></span>

<span data-ttu-id="91b85-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91b85-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91b85-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="91b85-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91b85-125">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91b85-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91b85-126">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="91b85-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91b85-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="91b85-127">Header files</span></span>

<span data-ttu-id="91b85-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91b85-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="91b85-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91b85-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91b85-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="91b85-130">See also</span></span>



[<span data-ttu-id="91b85-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="91b85-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91b85-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91b85-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91b85-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91b85-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91b85-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91b85-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

