---
title: PidNameKeywords の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameKeywords
api_type:
- COM
ms.assetid: bcc0cda0-02bc-49a5-9fb9-850b4c2867c1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b71579a4652df62e696cd0dc6113dde44fad4287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802338"
---
# <a name="pidnamekeywords-canonical-property"></a><span data-ttu-id="6ad5b-103">PidNameKeywords の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6ad5b-103">PidNameKeywords Canonical Property</span></span>

  
  
<span data-ttu-id="6ad5b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ad5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ad5b-105">キーワードやメッセージのオブジェクトのカテゴリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-105">Contains keywords or categories for the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ad5b-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="6ad5b-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="6ad5b-107">なし</span><span class="sxs-lookup"><span data-stu-id="6ad5b-107">None</span></span>  <br/> |
|<span data-ttu-id="6ad5b-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-108">Property set:</span></span>  <br/> |<span data-ttu-id="6ad5b-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="6ad5b-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="6ad5b-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="6ad5b-110">Property name:</span></span>  <br/> |<span data-ttu-id="6ad5b-111">キーワード</span><span class="sxs-lookup"><span data-stu-id="6ad5b-111">Keywords</span></span>  <br/> |
|<span data-ttu-id="6ad5b-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-112">Data type:</span></span>  <br/> |<span data-ttu-id="6ad5b-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ad5b-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6ad5b-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6ad5b-114">Area:</span></span>  <br/> |<span data-ttu-id="6ad5b-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="6ad5b-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ad5b-116">備考</span><span class="sxs-lookup"><span data-stu-id="6ad5b-116">Remarks</span></span>

<span data-ttu-id="6ad5b-117">メッセージのオブジェクトでは、このプロパティの複数値文字列内の各文字列の長さのカテゴリを指定する複数行文字列値は 256 未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-117">A multi-string value that specifies the categories for a message object, the length of each string within this property multi-value string, must be less than 256.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ad5b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6ad5b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ad5b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6ad5b-119">Protocol specifications</span></span>

<span data-ttu-id="6ad5b-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad5b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ad5b-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ad5b-122">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad5b-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ad5b-123">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-123">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6ad5b-124">[[MS OXODOC]](http://msdn.microsoft.com/library/103007c8-5066-4bed-84e3-4465907af098%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad5b-124">[[MS-OXODOC]](http://msdn.microsoft.com/library/103007c8-5066-4bed-84e3-4465907af098%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ad5b-125">プロパティは、ドキュメントに対する許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-125">Specifies the properties and operations that are permissible on documents.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ad5b-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6ad5b-126">Header files</span></span>

<span data-ttu-id="6ad5b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ad5b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ad5b-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ad5b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ad5b-129">See also</span></span>



[<span data-ttu-id="6ad5b-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ad5b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ad5b-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ad5b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ad5b-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6ad5b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ad5b-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6ad5b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

