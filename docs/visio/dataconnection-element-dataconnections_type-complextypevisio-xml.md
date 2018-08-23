---
title: DataConnection 要素 (DataConnections_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: 1 つまたは複数のデータ レコード セットの要素と XML 以外のデータ ソース間の通信を抽象化します。
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805174"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="70f33-103">DataConnection 要素 (DataConnections_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="70f33-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="70f33-104">1 つまたは複数の**データ レコード セット**の要素と XML 以外のデータ ソース間の通信を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="70f33-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="70f33-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="70f33-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70f33-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="70f33-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70f33-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="70f33-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70f33-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="70f33-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70f33-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="70f33-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70f33-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="70f33-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70f33-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="70f33-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70f33-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="70f33-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70f33-113">定義</span><span class="sxs-lookup"><span data-stu-id="70f33-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70f33-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="70f33-114">Elements and attributes</span></span>

<span data-ttu-id="70f33-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="70f33-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70f33-116">親要素</span><span class="sxs-lookup"><span data-stu-id="70f33-116">Parent elements</span></span>

|<span data-ttu-id="70f33-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="70f33-117">**Element**</span></span>|<span data-ttu-id="70f33-118">**型**</span><span class="sxs-lookup"><span data-stu-id="70f33-118">**Type**</span></span>|<span data-ttu-id="70f33-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="70f33-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70f33-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="70f33-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="70f33-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="70f33-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70f33-122">ドキュメントの**DataConnection**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="70f33-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70f33-123">子要素</span><span class="sxs-lookup"><span data-stu-id="70f33-123">Child elements</span></span>

<span data-ttu-id="70f33-124">なし。</span><span class="sxs-lookup"><span data-stu-id="70f33-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70f33-125">属性</span><span class="sxs-lookup"><span data-stu-id="70f33-125">Attributes</span></span>

|<span data-ttu-id="70f33-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="70f33-126">**Attribute**</span></span>|<span data-ttu-id="70f33-127">**型**</span><span class="sxs-lookup"><span data-stu-id="70f33-127">**Type**</span></span>|<span data-ttu-id="70f33-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="70f33-128">**Required**</span></span>|<span data-ttu-id="70f33-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="70f33-129">**Description**</span></span>|<span data-ttu-id="70f33-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="70f33-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70f33-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="70f33-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="70f33-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="70f33-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="70f33-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="70f33-133">optional</span></span>  <br/> |<span data-ttu-id="70f33-134">既定値は、false を指定します。</span><span class="sxs-lookup"><span data-stu-id="70f33-134">The default value is false.</span></span> <span data-ttu-id="70f33-135">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70f33-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="70f33-136">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="70f33-137">コマンド</span><span class="sxs-lookup"><span data-stu-id="70f33-137">Command</span></span>  <br/> |<span data-ttu-id="70f33-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70f33-138">xsd:string</span></span>  <br/> |<span data-ttu-id="70f33-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="70f33-139">optional</span></span>  <br/> |<span data-ttu-id="70f33-140">コマンド文字列は、データ ソースのクエリを実行するために使用します。</span><span class="sxs-lookup"><span data-stu-id="70f33-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="70f33-141">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70f33-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="70f33-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="70f33-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70f33-143">xsd:string</span></span>  <br/> |<span data-ttu-id="70f33-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="70f33-144">optional</span></span>  <br/> |<span data-ttu-id="70f33-145">データ ソースに接続するために必要なパラメーターを定義する接続文字列です。</span><span class="sxs-lookup"><span data-stu-id="70f33-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="70f33-146">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70f33-147">FileName</span><span class="sxs-lookup"><span data-stu-id="70f33-147">FileName</span></span>  <br/> |<span data-ttu-id="70f33-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70f33-148">xsd:string</span></span>  <br/> |<span data-ttu-id="70f33-149">必須</span><span class="sxs-lookup"><span data-stu-id="70f33-149">required</span></span>  <br/> |<span data-ttu-id="70f33-150">接続ファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="70f33-150">The name of the connection file.</span></span> <span data-ttu-id="70f33-151">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70f33-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="70f33-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70f33-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="70f33-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="70f33-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70f33-154">xsd:string</span></span>  <br/> |<span data-ttu-id="70f33-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="70f33-155">optional</span></span>  <br/> |<span data-ttu-id="70f33-156">ユーザーは、データ接続の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="70f33-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="70f33-157">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70f33-158">ID</span><span class="sxs-lookup"><span data-stu-id="70f33-158">ID</span></span>  <br/> |<span data-ttu-id="70f33-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70f33-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70f33-160">必須</span><span class="sxs-lookup"><span data-stu-id="70f33-160">required</span></span>  <br/> |<span data-ttu-id="70f33-161">Visio で指定された接続では、ドキュメント内で一意に割り当てられた ID です。</span><span class="sxs-lookup"><span data-stu-id="70f33-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="70f33-162">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70f33-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="70f33-163">Timeout</span></span>  <br/> |<span data-ttu-id="70f33-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70f33-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70f33-165">省略可能</span><span class="sxs-lookup"><span data-stu-id="70f33-165">optional</span></span>  <br/> |<span data-ttu-id="70f33-166">試行を終了する前に接続を確立しようとしているときに分単位での待機時間です。</span><span class="sxs-lookup"><span data-stu-id="70f33-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="70f33-167">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70f33-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

