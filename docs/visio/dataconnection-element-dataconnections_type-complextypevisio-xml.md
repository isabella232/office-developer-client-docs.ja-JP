---
title: DataConnection 要素 (DataConnections_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: 1つまたは複数の DataRecordset 要素と非 XML データソース間の情報を抽出します。
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344626"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="db99b-103">DataConnection 要素 (DataConnections_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="db99b-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="db99b-104">1つまたは複数の**DataRecordset**要素と非 XML データソース間の情報を抽出します。</span><span class="sxs-lookup"><span data-stu-id="db99b-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="db99b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="db99b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db99b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="db99b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="db99b-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="db99b-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="db99b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db99b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="db99b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="db99b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="db99b-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="db99b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="db99b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="db99b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="db99b-112">接続 xml</span><span class="sxs-lookup"><span data-stu-id="db99b-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db99b-113">定義</span><span class="sxs-lookup"><span data-stu-id="db99b-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="db99b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="db99b-114">Elements and attributes</span></span>

<span data-ttu-id="db99b-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="db99b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="db99b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="db99b-116">Parent elements</span></span>

|<span data-ttu-id="db99b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="db99b-117">**Element**</span></span>|<span data-ttu-id="db99b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="db99b-118">**Type**</span></span>|<span data-ttu-id="db99b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="db99b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db99b-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="db99b-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="db99b-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="db99b-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="db99b-122">文書の**DataConnection**要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="db99b-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="db99b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="db99b-123">Child elements</span></span>

<span data-ttu-id="db99b-124">なし。</span><span class="sxs-lookup"><span data-stu-id="db99b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db99b-125">属性</span><span class="sxs-lookup"><span data-stu-id="db99b-125">Attributes</span></span>

|<span data-ttu-id="db99b-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="db99b-126">**Attribute**</span></span>|<span data-ttu-id="db99b-127">**型**</span><span class="sxs-lookup"><span data-stu-id="db99b-127">**Type**</span></span>|<span data-ttu-id="db99b-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="db99b-128">**Required**</span></span>|<span data-ttu-id="db99b-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="db99b-129">**Description**</span></span>|<span data-ttu-id="db99b-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="db99b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="db99b-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="db99b-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="db99b-132">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="db99b-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="db99b-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="db99b-133">optional</span></span>  <br/> |<span data-ttu-id="db99b-134">既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="db99b-134">The default value is false.</span></span> <span data-ttu-id="db99b-135">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db99b-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="db99b-136">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="db99b-137">Command</span><span class="sxs-lookup"><span data-stu-id="db99b-137">Command</span></span>  <br/> |<span data-ttu-id="db99b-138">xsd: string</span><span class="sxs-lookup"><span data-stu-id="db99b-138">xsd:string</span></span>  <br/> |<span data-ttu-id="db99b-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="db99b-139">optional</span></span>  <br/> |<span data-ttu-id="db99b-140">データソースのクエリに使用されるコマンド文字列。</span><span class="sxs-lookup"><span data-stu-id="db99b-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="db99b-141">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db99b-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="db99b-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="db99b-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="db99b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="db99b-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="db99b-144">optional</span></span>  <br/> |<span data-ttu-id="db99b-145">データソースへの接続に必要なパラメーターを定義する接続文字列。</span><span class="sxs-lookup"><span data-stu-id="db99b-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="db99b-146">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db99b-147">FileName</span><span class="sxs-lookup"><span data-stu-id="db99b-147">FileName</span></span>  <br/> |<span data-ttu-id="db99b-148">xsd: string</span><span class="sxs-lookup"><span data-stu-id="db99b-148">xsd:string</span></span>  <br/> |<span data-ttu-id="db99b-149">必須</span><span class="sxs-lookup"><span data-stu-id="db99b-149">required</span></span>  <br/> |<span data-ttu-id="db99b-150">接続ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="db99b-150">The name of the connection file.</span></span> <span data-ttu-id="db99b-151">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db99b-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="db99b-152">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db99b-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="db99b-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="db99b-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="db99b-154">xsd:string</span></span>  <br/> |<span data-ttu-id="db99b-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="db99b-155">optional</span></span>  <br/> |<span data-ttu-id="db99b-156">ユーザーが入力したデータ接続の名前。</span><span class="sxs-lookup"><span data-stu-id="db99b-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="db99b-157">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db99b-158">ID</span><span class="sxs-lookup"><span data-stu-id="db99b-158">ID</span></span>  <br/> |<span data-ttu-id="db99b-159">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="db99b-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db99b-160">必須</span><span class="sxs-lookup"><span data-stu-id="db99b-160">required</span></span>  <br/> |<span data-ttu-id="db99b-161">指定された接続に対して Visio によって割り当てられた ID。ドキュメント内で一意です。</span><span class="sxs-lookup"><span data-stu-id="db99b-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="db99b-162">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="db99b-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="db99b-163">Timeout</span></span>  <br/> |<span data-ttu-id="db99b-164">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="db99b-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db99b-165">省略可能</span><span class="sxs-lookup"><span data-stu-id="db99b-165">optional</span></span>  <br/> |<span data-ttu-id="db99b-166">試行を終了する前に接続を確立しようとしている間の待機時間 (分単位)。</span><span class="sxs-lookup"><span data-stu-id="db99b-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="db99b-167">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="db99b-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

