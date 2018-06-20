---
title: PidTagRoamingDatatypes の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803367"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="241b0-103">PidTagRoamingDatatypes の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="241b0-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="241b0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="241b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="241b0-105">プロパティがメッセージに存在するストリームを示すビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="241b0-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="241b0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="241b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="241b0-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="241b0-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="241b0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="241b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="241b0-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="241b0-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="241b0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="241b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="241b0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="241b0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="241b0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="241b0-112">Area:</span></span>  <br/> |<span data-ttu-id="241b0-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="241b0-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="241b0-114">備考</span><span class="sxs-lookup"><span data-stu-id="241b0-114">Remarks</span></span>

<span data-ttu-id="241b0-115">このプロパティは、次の値の 1 つ以上に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="241b0-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="241b0-116">**値**</span><span class="sxs-lookup"><span data-stu-id="241b0-116">**Value**</span></span>|<span data-ttu-id="241b0-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="241b0-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="241b0-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="241b0-118">0x00000002</span></span>  <br/> |<span data-ttu-id="241b0-119">フォルダー関連情報 (FAI) メッセージに固定の XML スキーマとしてシリアル化され、 **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) のプロパティに格納されている辞書のストリームが含まれている必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="241b0-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="241b0-120">FAI メッセージに辞書のストリームが含まれていない場合、アプリケーションは、エントリがないものとして、辞書を扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="241b0-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="241b0-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="241b0-121">0x00000004</span></span>  <br/> |<span data-ttu-id="241b0-122">FAI メッセージに任意の XML スキーマを使用する**PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) のプロパティに格納されている XML ストリームが含まれている必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="241b0-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="241b0-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="241b0-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="241b0-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="241b0-124">Protocol specifications</span></span>

<span data-ttu-id="241b0-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="241b0-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="241b0-126">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="241b0-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="241b0-127">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="241b0-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="241b0-128">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="241b0-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="241b0-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="241b0-129">Header files</span></span>

<span data-ttu-id="241b0-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="241b0-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="241b0-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="241b0-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="241b0-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="241b0-132">Mapitags.h</span></span>
  
> <span data-ttu-id="241b0-133">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="241b0-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="241b0-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="241b0-134">See also</span></span>



[<span data-ttu-id="241b0-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="241b0-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="241b0-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="241b0-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="241b0-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="241b0-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="241b0-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="241b0-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

