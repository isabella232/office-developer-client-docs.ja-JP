---
title: PidLidVerbResponse の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidVerbResponse
api_type:
- COM
ms.assetid: 6f3db5ac-f1cb-4c55-ab88-c126dd5f48ee
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 267fcc2b6f8902b1f9abb7adcd4409875fc1a7b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802278"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="97399-103">PidLidVerbResponse の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="97399-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="97399-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97399-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97399-105">回答者が選択した返信のオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="97399-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97399-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="97399-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97399-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="97399-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="97399-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="97399-108">Property set:</span></span>  <br/> |<span data-ttu-id="97399-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="97399-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="97399-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="97399-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="97399-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="97399-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="97399-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="97399-112">Data type:</span></span>  <br/> |<span data-ttu-id="97399-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97399-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="97399-114">領域:</span><span class="sxs-lookup"><span data-stu-id="97399-114">Area:</span></span>  <br/> |<span data-ttu-id="97399-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="97399-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97399-116">備考</span><span class="sxs-lookup"><span data-stu-id="97399-116">Remarks</span></span>

<span data-ttu-id="97399-117">このプロパティは通常、回答者が投票する**dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) のプロパティに含まれる区切られた値のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="97399-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97399-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="97399-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97399-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="97399-119">Protocol specifications</span></span>

<span data-ttu-id="97399-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97399-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97399-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="97399-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97399-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97399-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97399-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="97399-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97399-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="97399-124">Header files</span></span>

<span data-ttu-id="97399-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97399-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="97399-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="97399-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97399-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="97399-127">See also</span></span>



[<span data-ttu-id="97399-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="97399-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97399-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="97399-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97399-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="97399-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97399-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="97399-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

