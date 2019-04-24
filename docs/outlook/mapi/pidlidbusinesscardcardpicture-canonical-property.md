---
title: PidLidBusinessCardCardPicture 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342008"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="3e421-103">PidLidBusinessCardCardPicture 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e421-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="3e421-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e421-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e421-105">名刺で使用する画像が保存されています。</span><span class="sxs-lookup"><span data-stu-id="3e421-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e421-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3e421-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e421-107">dispidbccardpicture</span><span class="sxs-lookup"><span data-stu-id="3e421-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="3e421-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="3e421-108">Property set:</span></span>  <br/> |<span data-ttu-id="3e421-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3e421-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3e421-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3e421-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3e421-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="3e421-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="3e421-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3e421-112">Data type:</span></span>  <br/> |<span data-ttu-id="3e421-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3e421-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3e421-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="3e421-114">Area:</span></span>  <br/> |<span data-ttu-id="3e421-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="3e421-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e421-116">解説</span><span class="sxs-lookup"><span data-stu-id="3e421-116">Remarks</span></span>

<span data-ttu-id="3e421-117">このプロパティの値は、ポータブルネットワークグラフィックス (PNG) または JPEG ストリームのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e421-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="3e421-118">このプロパティは、 **dispidbcdisplaydefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) プロパティと共に使用する必要があります。 **dispidbcdisplaydefinition**が連絡先に存在しない場合**は、次のようにします。dispidbcdisplaydefinition**が存在しません。</span><span class="sxs-lookup"><span data-stu-id="3e421-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="3e421-119">このプロパティは、 **dispidbccardpicture**のデータがカードイメージを必要としない場合にも存在しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e421-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3e421-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3e421-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e421-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3e421-121">Protocol specifications</span></span>

<span data-ttu-id="3e421-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e421-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e421-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e421-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e421-124">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e421-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e421-125">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e421-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e421-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3e421-126">Header files</span></span>

<span data-ttu-id="3e421-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e421-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e421-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e421-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e421-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e421-129">See also</span></span>



[<span data-ttu-id="3e421-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3e421-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e421-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e421-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e421-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3e421-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e421-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3e421-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

