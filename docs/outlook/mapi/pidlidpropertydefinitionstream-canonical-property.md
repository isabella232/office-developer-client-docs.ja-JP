---
title: PidLidPropertyDefinitionStream の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802092"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="484ed-103">PidLidPropertyDefinitionStream の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="484ed-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="484ed-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="484ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="484ed-105">ユーザー定義のフィールドの定義と、メッセージの組み込みのフィールドのデータ バインディングの設定を表します。</span><span class="sxs-lookup"><span data-stu-id="484ed-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="484ed-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="484ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="484ed-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="484ed-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="484ed-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="484ed-108">Property set:</span></span>  <br/> |<span data-ttu-id="484ed-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="484ed-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="484ed-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="484ed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="484ed-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="484ed-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="484ed-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="484ed-112">Data type:</span></span>  <br/> |<span data-ttu-id="484ed-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="484ed-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="484ed-114">領域:</span><span class="sxs-lookup"><span data-stu-id="484ed-114">Area:</span></span>  <br/> |<span data-ttu-id="484ed-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="484ed-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="484ed-116">備考</span><span class="sxs-lookup"><span data-stu-id="484ed-116">Remarks</span></span>

<span data-ttu-id="484ed-117">**PidLidPropertyDefinitionStream**プロパティの値は、メッセージのユーザー設定フォームの定義の一部として保存されます。</span><span class="sxs-lookup"><span data-stu-id="484ed-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="484ed-118">このプロパティの値は、バイナリ ストリームです。</span><span class="sxs-lookup"><span data-stu-id="484ed-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="484ed-119">このストリームの構造については、 [PropertyDefinition ストリームの構造体](propertydefinition-stream-structure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="484ed-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="484ed-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="484ed-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="484ed-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="484ed-121">Protocol specifications</span></span>

<span data-ttu-id="484ed-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="484ed-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="484ed-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="484ed-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="484ed-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="484ed-124">Header files</span></span>

<span data-ttu-id="484ed-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="484ed-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="484ed-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="484ed-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="484ed-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="484ed-127">See also</span></span>



[<span data-ttu-id="484ed-128">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="484ed-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="484ed-129">新しいユーザー定義フィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="484ed-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="484ed-130">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="484ed-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="484ed-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="484ed-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="484ed-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="484ed-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="484ed-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="484ed-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="484ed-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="484ed-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

