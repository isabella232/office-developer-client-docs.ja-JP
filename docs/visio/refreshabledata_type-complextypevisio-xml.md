---
title: RefreshableData_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d715737a-1daa-4c61-e1c6-c997b1b71302
ms.openlocfilehash: 6313799e6be26720e9d6c3b5677ca0ab3783e6b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346467"
---
# <a name="refreshabledatatype-complextype-visio-xml"></a><span data-ttu-id="03b40-102">RefreshableData_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="03b40-102">RefreshableData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="03b40-103">型情報</span><span class="sxs-lookup"><span data-stu-id="03b40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03b40-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="03b40-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="03b40-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="03b40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="03b40-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="03b40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="03b40-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="03b40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="03b40-108">なし</span><span class="sxs-lookup"><span data-stu-id="03b40-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="03b40-109">定義</span><span class="sxs-lookup"><span data-stu-id="03b40-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshableData_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="03b40-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="03b40-110">Elements and attributes</span></span>

<span data-ttu-id="03b40-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="03b40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="03b40-112">子要素</span><span class="sxs-lookup"><span data-stu-id="03b40-112">Child elements</span></span>

<span data-ttu-id="03b40-113">なし。</span><span class="sxs-lookup"><span data-stu-id="03b40-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03b40-114">属性</span><span class="sxs-lookup"><span data-stu-id="03b40-114">Attributes</span></span>

|<span data-ttu-id="03b40-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="03b40-115">**Attribute**</span></span>|<span data-ttu-id="03b40-116">**型**</span><span class="sxs-lookup"><span data-stu-id="03b40-116">**Type**</span></span>|<span data-ttu-id="03b40-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="03b40-117">**Required**</span></span>|<span data-ttu-id="03b40-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="03b40-118">**Description**</span></span>|<span data-ttu-id="03b40-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="03b40-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="03b40-120">ID</span><span class="sxs-lookup"><span data-stu-id="03b40-120">ID</span></span>  <br/> |<span data-ttu-id="03b40-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="03b40-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03b40-122">必須</span><span class="sxs-lookup"><span data-stu-id="03b40-122">required</span></span>  <br/> ||<span data-ttu-id="03b40-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="03b40-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

