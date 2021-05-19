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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342036"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="5026a-103">PidLidBusinessCardDisplayDefinition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5026a-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="5026a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5026a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5026a-105">連絡先を名刺として表示するためのユーザーカスタマイズの詳細が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5026a-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5026a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5026a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5026a-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="5026a-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="5026a-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="5026a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5026a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5026a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5026a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5026a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5026a-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="5026a-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="5026a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5026a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5026a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5026a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5026a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5026a-114">Area:</span></span>  <br/> |<span data-ttu-id="5026a-115">Contact</span><span class="sxs-lookup"><span data-stu-id="5026a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5026a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5026a-116">Remarks</span></span>

<span data-ttu-id="5026a-117">名刺のレイアウトは、画像と多数のテキスト フィールドとして表されます。</span><span class="sxs-lookup"><span data-stu-id="5026a-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="5026a-118">画像には、連絡先写真またはカード画像を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5026a-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="5026a-119">テキスト フィールドは、連絡先の別のプロパティ セットの値と、ユーザーが提供するオプションのカスタマイズされたラベル文字列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="5026a-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="5026a-120">マルチバイト値は、バッファーにリトル エンド形式で格納されます。</span><span class="sxs-lookup"><span data-stu-id="5026a-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5026a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5026a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5026a-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5026a-122">Protocol specifications</span></span>

<span data-ttu-id="5026a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5026a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5026a-124">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5026a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5026a-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5026a-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5026a-126">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5026a-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5026a-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5026a-127">Header files</span></span>

<span data-ttu-id="5026a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5026a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5026a-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5026a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5026a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5026a-130">See also</span></span>



[<span data-ttu-id="5026a-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5026a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5026a-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5026a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5026a-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5026a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5026a-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5026a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

