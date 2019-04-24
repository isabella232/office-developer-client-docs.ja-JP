---
title: PidTagRoamingDatatypes 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359557"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="a0e82-103">PidTagRoamingDatatypes 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0e82-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="a0e82-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0e82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0e82-105">メッセージに存在するストリームプロパティを示すビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="a0e82-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0e82-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a0e82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0e82-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="a0e82-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="a0e82-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a0e82-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0e82-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="a0e82-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="a0e82-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a0e82-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0e82-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a0e82-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a0e82-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a0e82-112">Area:</span></span>  <br/> |<span data-ttu-id="a0e82-113">構成</span><span class="sxs-lookup"><span data-stu-id="a0e82-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0e82-114">解説</span><span class="sxs-lookup"><span data-stu-id="a0e82-114">Remarks</span></span>

<span data-ttu-id="a0e82-115">このプロパティは、次のいずれかまたは複数の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0e82-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="a0e82-116">**値**</span><span class="sxs-lookup"><span data-stu-id="a0e82-116">**Value**</span></span>|<span data-ttu-id="a0e82-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="a0e82-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0e82-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a0e82-118">0x00000002</span></span>  <br/> |<span data-ttu-id="a0e82-119">フォルダーに関連付けられた情報 (fai) メッセージに、 **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) プロパティに格納された、固定の XML スキーマにシリアル化された辞書ストリームを含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="a0e82-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="a0e82-120">fai メッセージに辞書ストリームが含まれていない場合、アプリケーションでは、エントリを持たない辞書として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0e82-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="a0e82-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a0e82-121">0x00000004</span></span>  <br/> |<span data-ttu-id="a0e82-122">任意の xml スキーマを使用する**PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) プロパティに格納されている xml ストリームを fai メッセージに含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="a0e82-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a0e82-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a0e82-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0e82-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a0e82-124">Protocol specifications</span></span>

<span data-ttu-id="a0e82-125">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0e82-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0e82-126">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0e82-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0e82-127">[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0e82-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0e82-128">カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a0e82-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0e82-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a0e82-129">Header files</span></span>

<span data-ttu-id="a0e82-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0e82-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0e82-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0e82-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0e82-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a0e82-132">Mapitags.h</span></span>
  
> <span data-ttu-id="a0e82-133">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0e82-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0e82-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0e82-134">See also</span></span>



[<span data-ttu-id="a0e82-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a0e82-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0e82-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0e82-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0e82-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a0e82-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0e82-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a0e82-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

