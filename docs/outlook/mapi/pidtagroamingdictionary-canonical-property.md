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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400328"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="05aec-103">PidTagRoamingDictionary 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05aec-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="05aec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05aec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05aec-105">移動の辞書を記述する XML ドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="05aec-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05aec-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="05aec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05aec-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="05aec-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="05aec-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="05aec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05aec-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="05aec-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="05aec-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="05aec-110">Data type:</span></span>  <br/> |<span data-ttu-id="05aec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="05aec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="05aec-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="05aec-112">Area:</span></span>  <br/> |<span data-ttu-id="05aec-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="05aec-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05aec-114">備考</span><span class="sxs-lookup"><span data-stu-id="05aec-114">Remarks</span></span>

<span data-ttu-id="05aec-115">このプロパティには、UTF8 エンコーディングを使用している UNICODE XML ドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="05aec-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="05aec-116">辞書のストリームを持つメッセージは、次のスキーマでは、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05aec-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
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

<span data-ttu-id="05aec-117">構成データ メッセージには、このプロパティに格納されている XML ドキュメントのサンプルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="05aec-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
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

## <a name="related-resources"></a><span data-ttu-id="05aec-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05aec-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05aec-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="05aec-119">Protocol specifications</span></span>

<span data-ttu-id="05aec-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05aec-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05aec-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="05aec-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05aec-122">[[MS OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05aec-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05aec-123">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="05aec-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05aec-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="05aec-124">Header files</span></span>

<span data-ttu-id="05aec-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05aec-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="05aec-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05aec-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="05aec-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05aec-127">Mapitags.h</span></span>
  
> <span data-ttu-id="05aec-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05aec-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05aec-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="05aec-129">See also</span></span>



[<span data-ttu-id="05aec-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05aec-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05aec-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05aec-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05aec-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05aec-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05aec-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05aec-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

