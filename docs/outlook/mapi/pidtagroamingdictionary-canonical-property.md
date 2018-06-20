---
title: PidTagRoamingDictionary の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803380"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="cb1c9-103">PidTagRoamingDictionary の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cb1c9-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="cb1c9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb1c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb1c9-105">移動の辞書を記述する XML ドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb1c9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb1c9-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="cb1c9-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="cb1c9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cb1c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb1c9-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="cb1c9-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="cb1c9-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb1c9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb1c9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cb1c9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cb1c9-112">Area:</span></span>  <br/> |<span data-ttu-id="cb1c9-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="cb1c9-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb1c9-114">備考</span><span class="sxs-lookup"><span data-stu-id="cb1c9-114">Remarks</span></span>

<span data-ttu-id="cb1c9-115">このプロパティには、UTF8 エンコーディングを使用している UNICODE XML ドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="cb1c9-116">辞書のストリームを持つメッセージは、次のスキーマでは、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
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

<span data-ttu-id="cb1c9-117">構成データ メッセージには、このプロパティに格納されている XML ドキュメントのサンプルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
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

## <a name="related-resources"></a><span data-ttu-id="cb1c9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cb1c9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb1c9-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cb1c9-119">Protocol specifications</span></span>

<span data-ttu-id="cb1c9-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb1c9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb1c9-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb1c9-122">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb1c9-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb1c9-123">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb1c9-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cb1c9-124">Header files</span></span>

<span data-ttu-id="cb1c9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb1c9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb1c9-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb1c9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb1c9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cb1c9-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb1c9-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb1c9-129">See also</span></span>



[<span data-ttu-id="cb1c9-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb1c9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb1c9-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb1c9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb1c9-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cb1c9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb1c9-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cb1c9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

