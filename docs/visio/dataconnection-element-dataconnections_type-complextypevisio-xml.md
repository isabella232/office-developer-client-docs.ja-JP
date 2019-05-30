---
title: DataConnection 要素 (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: 1つまたは複数の DataRecordset 要素と非 XML データソース間の情報を抽出します。
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538404"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="427cb-103">DataConnection 要素 (DataConnections_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="427cb-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="427cb-104">1つまたは複数の**DataRecordset**要素と非 XML データソース間の情報を抽出します。</span><span class="sxs-lookup"><span data-stu-id="427cb-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="427cb-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="427cb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="427cb-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="427cb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="427cb-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="427cb-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="427cb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="427cb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="427cb-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="427cb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="427cb-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="427cb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="427cb-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="427cb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="427cb-112">接続 xml</span><span class="sxs-lookup"><span data-stu-id="427cb-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="427cb-113">定義</span><span class="sxs-lookup"><span data-stu-id="427cb-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="427cb-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="427cb-114">Elements and attributes</span></span>

<span data-ttu-id="427cb-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="427cb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="427cb-116">親要素</span><span class="sxs-lookup"><span data-stu-id="427cb-116">Parent elements</span></span>

|<span data-ttu-id="427cb-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="427cb-117">**Element**</span></span>|<span data-ttu-id="427cb-118">**型**</span><span class="sxs-lookup"><span data-stu-id="427cb-118">**Type**</span></span>|<span data-ttu-id="427cb-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="427cb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="427cb-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="427cb-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="427cb-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="427cb-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="427cb-122">文書の**DataConnection**要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="427cb-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="427cb-123">子要素</span><span class="sxs-lookup"><span data-stu-id="427cb-123">Child elements</span></span>

<span data-ttu-id="427cb-124">なし。</span><span class="sxs-lookup"><span data-stu-id="427cb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="427cb-125">属性</span><span class="sxs-lookup"><span data-stu-id="427cb-125">Attributes</span></span>

|<span data-ttu-id="427cb-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="427cb-126">**Attribute**</span></span>|<span data-ttu-id="427cb-127">**型**</span><span class="sxs-lookup"><span data-stu-id="427cb-127">**Type**</span></span>|<span data-ttu-id="427cb-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="427cb-128">**Required**</span></span>|<span data-ttu-id="427cb-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="427cb-129">**Description**</span></span>|<span data-ttu-id="427cb-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="427cb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="427cb-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="427cb-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="427cb-132">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="427cb-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="427cb-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="427cb-133">optional</span></span>  <br/> |<span data-ttu-id="427cb-134">既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="427cb-134">The default value is false.</span></span> <span data-ttu-id="427cb-135">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="427cb-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="427cb-136">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="427cb-137">Command</span><span class="sxs-lookup"><span data-stu-id="427cb-137">Command</span></span>  <br/> |<span data-ttu-id="427cb-138">xsd: string</span><span class="sxs-lookup"><span data-stu-id="427cb-138">xsd:string</span></span>  <br/> |<span data-ttu-id="427cb-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="427cb-139">optional</span></span>  <br/> |<span data-ttu-id="427cb-140">データソースのクエリに使用されるコマンド文字列。</span><span class="sxs-lookup"><span data-stu-id="427cb-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="427cb-141">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="427cb-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="427cb-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="427cb-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="427cb-143">xsd:string</span></span>  <br/> |<span data-ttu-id="427cb-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="427cb-144">optional</span></span>  <br/> |<span data-ttu-id="427cb-145">データソースへの接続に必要なパラメーターを定義する接続文字列。</span><span class="sxs-lookup"><span data-stu-id="427cb-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="427cb-146">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="427cb-147">FileName</span><span class="sxs-lookup"><span data-stu-id="427cb-147">FileName</span></span>  <br/> |<span data-ttu-id="427cb-148">xsd: string</span><span class="sxs-lookup"><span data-stu-id="427cb-148">xsd:string</span></span>  <br/> |<span data-ttu-id="427cb-149">必須</span><span class="sxs-lookup"><span data-stu-id="427cb-149">required</span></span>  <br/> |<span data-ttu-id="427cb-150">接続ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="427cb-150">The name of the connection file.</span></span> <span data-ttu-id="427cb-151">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="427cb-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="427cb-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="427cb-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="427cb-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="427cb-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="427cb-154">xsd:string</span></span>  <br/> |<span data-ttu-id="427cb-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="427cb-155">optional</span></span>  <br/> |<span data-ttu-id="427cb-156">ユーザーが入力したデータ接続の名前。</span><span class="sxs-lookup"><span data-stu-id="427cb-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="427cb-157">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="427cb-158">ID</span><span class="sxs-lookup"><span data-stu-id="427cb-158">ID</span></span>  <br/> |<span data-ttu-id="427cb-159">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="427cb-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="427cb-160">必須</span><span class="sxs-lookup"><span data-stu-id="427cb-160">required</span></span>  <br/> |<span data-ttu-id="427cb-161">指定された接続に対して Visio によって割り当てられた ID。ドキュメント内で一意です。</span><span class="sxs-lookup"><span data-stu-id="427cb-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="427cb-162">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="427cb-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="427cb-163">Timeout</span></span>  <br/> |<span data-ttu-id="427cb-164">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="427cb-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="427cb-165">省略可能</span><span class="sxs-lookup"><span data-stu-id="427cb-165">optional</span></span>  <br/> |<span data-ttu-id="427cb-166">試行を終了する前に接続を確立しようとしている間の待機時間 (分単位)。</span><span class="sxs-lookup"><span data-stu-id="427cb-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="427cb-167">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="427cb-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

