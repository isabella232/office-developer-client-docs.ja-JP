---
title: PidTagRoamingDictionary 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359550"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="8105b-103">PidTagRoamingDictionary 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8105b-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="8105b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8105b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8105b-105">ローミング ディクショナリを記述する XML ドキュメントが含まれる。</span><span class="sxs-lookup"><span data-stu-id="8105b-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8105b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8105b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8105b-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="8105b-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="8105b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8105b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8105b-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="8105b-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="8105b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8105b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8105b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8105b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8105b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8105b-112">Area:</span></span>  <br/> |<span data-ttu-id="8105b-113">構成</span><span class="sxs-lookup"><span data-stu-id="8105b-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8105b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8105b-114">Remarks</span></span>

<span data-ttu-id="8105b-115">このプロパティには、UTF8 エンコードを使用している UNICODE XML ドキュメントが含まれる。</span><span class="sxs-lookup"><span data-stu-id="8105b-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="8105b-116">辞書ストリームを含むメッセージは、次のスキーマでこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8105b-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="https://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="8105b-117">構成データ メッセージにこのプロパティに格納されている XML ドキュメントの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8105b-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="8105b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8105b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8105b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8105b-119">Protocol specifications</span></span>

<span data-ttu-id="8105b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8105b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8105b-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="8105b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8105b-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8105b-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8105b-123">共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="8105b-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8105b-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8105b-124">Header files</span></span>

<span data-ttu-id="8105b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8105b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8105b-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8105b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8105b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8105b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8105b-128">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8105b-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8105b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="8105b-129">See also</span></span>



[<span data-ttu-id="8105b-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8105b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8105b-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8105b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8105b-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8105b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8105b-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8105b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

