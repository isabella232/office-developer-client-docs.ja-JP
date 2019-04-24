---
title: PidLidPropertyDefinitionStream 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315940"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="c996f-103">PidLidPropertyDefinitionStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c996f-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="c996f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c996f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c996f-105">ユーザー定義のフィールドと、メッセージの組み込みフィールドのデータバインド設定の定義を表します。</span><span class="sxs-lookup"><span data-stu-id="c996f-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c996f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c996f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c996f-107">dispidpropdefstream</span><span class="sxs-lookup"><span data-stu-id="c996f-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="c996f-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="c996f-108">Property set:</span></span>  <br/> |<span data-ttu-id="c996f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c996f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c996f-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c996f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c996f-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="c996f-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="c996f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c996f-112">Data type:</span></span>  <br/> |<span data-ttu-id="c996f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c996f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c996f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c996f-114">Area:</span></span>  <br/> |<span data-ttu-id="c996f-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="c996f-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c996f-116">解説</span><span class="sxs-lookup"><span data-stu-id="c996f-116">Remarks</span></span>

<span data-ttu-id="c996f-117">**PidLidPropertyDefinitionStream**プロパティの値は、メッセージのカスタムフォーム定義の一部として保存されます。</span><span class="sxs-lookup"><span data-stu-id="c996f-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="c996f-118">このプロパティの値は、バイナリストリームです。</span><span class="sxs-lookup"><span data-stu-id="c996f-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="c996f-119">このストリームの構造の詳細については、「 [propertydefinition stream structure](propertydefinition-stream-structure.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c996f-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c996f-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c996f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c996f-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c996f-121">Protocol specifications</span></span>

<span data-ttu-id="c996f-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c996f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c996f-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c996f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c996f-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c996f-124">Header files</span></span>

<span data-ttu-id="c996f-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c996f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c996f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c996f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c996f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c996f-127">See also</span></span>



[<span data-ttu-id="c996f-128">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="c996f-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="c996f-129">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="c996f-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="c996f-130">propertydefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="c996f-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="c996f-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c996f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c996f-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c996f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c996f-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c996f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c996f-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c996f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

