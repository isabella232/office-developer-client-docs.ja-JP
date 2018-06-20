---
title: DataConnections_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 57781566bd94a057faaae719d02b13154ad6de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805163"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="394db-102">DataConnections_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="394db-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="394db-103">型情報</span><span class="sxs-lookup"><span data-stu-id="394db-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="394db-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="394db-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="394db-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="394db-105">**Schema file**</span></span> <br/> |<span data-ttu-id="394db-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="394db-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="394db-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="394db-107">**Extension base**</span></span> <br/> |<span data-ttu-id="394db-108">なし</span><span class="sxs-lookup"><span data-stu-id="394db-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="394db-109">定義</span><span class="sxs-lookup"><span data-stu-id="394db-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="394db-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="394db-110">Elements and attributes</span></span>

<span data-ttu-id="394db-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="394db-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="394db-112">子要素</span><span class="sxs-lookup"><span data-stu-id="394db-112">Child elements</span></span>

|<span data-ttu-id="394db-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="394db-113">**Element**</span></span>|<span data-ttu-id="394db-114">**型**</span><span class="sxs-lookup"><span data-stu-id="394db-114">**Type**</span></span>|<span data-ttu-id="394db-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="394db-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="394db-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="394db-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="394db-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="394db-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="394db-118">属性</span><span class="sxs-lookup"><span data-stu-id="394db-118">Attributes</span></span>

|<span data-ttu-id="394db-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="394db-119">**Attribute**</span></span>|<span data-ttu-id="394db-120">**型**</span><span class="sxs-lookup"><span data-stu-id="394db-120">**Type**</span></span>|<span data-ttu-id="394db-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="394db-121">**Required**</span></span>|<span data-ttu-id="394db-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="394db-122">**Description**</span></span>|<span data-ttu-id="394db-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="394db-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="394db-124">NextID</span><span class="sxs-lookup"><span data-stu-id="394db-124">NextID</span></span>  <br/> |<span data-ttu-id="394db-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="394db-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="394db-126">必須</span><span class="sxs-lookup"><span data-stu-id="394db-126">required</span></span>  <br/> ||<span data-ttu-id="394db-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="394db-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

