---
title: 名前空間 (アクセスのデスクトップのデータベース参照)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef37f04ec6824cedf773cb72751b2364d2b3edf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876562"
---
# <a name="namespaces"></a><span data-ttu-id="186f9-102">名前空間</span><span class="sxs-lookup"><span data-stu-id="186f9-102">Namespaces</span></span>


<span data-ttu-id="186f9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="186f9-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="namespaces"></a><span data-ttu-id="186f9-104">名前空間</span><span class="sxs-lookup"><span data-stu-id="186f9-104">Namespaces</span></span>

<span data-ttu-id="186f9-105">ADO での XML の保存形式には、次の 4 つの名前空間が使用されます。</span><span class="sxs-lookup"><span data-stu-id="186f9-105">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="186f9-106">接頭語</span><span class="sxs-lookup"><span data-stu-id="186f9-106">Prefix</span></span></p></th>
<th><p><span data-ttu-id="186f9-107">説明</span><span class="sxs-lookup"><span data-stu-id="186f9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="186f9-108">s</span><span class="sxs-lookup"><span data-stu-id="186f9-108">s</span></span></p></td>
<td><p><span data-ttu-id="186f9-109">参照して、 &quot;XML データ&quot;名前空間の要素と現在の<strong>レコード セット</strong>のスキーマを定義する属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="186f9-109">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186f9-110">dt</span><span class="sxs-lookup"><span data-stu-id="186f9-110">dt</span></span></p></td>
<td><p><span data-ttu-id="186f9-111">データ型定義の仕様を表します。</span><span class="sxs-lookup"><span data-stu-id="186f9-111">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="186f9-112">rs</span><span class="sxs-lookup"><span data-stu-id="186f9-112">rs</span></span></p></td>
<td><p><span data-ttu-id="186f9-113">ADO の <strong>Recordset</strong> プロパティおよび属性に固有の要素と属性を含む名前空間を表します。</span><span class="sxs-lookup"><span data-stu-id="186f9-113">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186f9-114">z</span><span class="sxs-lookup"><span data-stu-id="186f9-114">z</span></span></p></td>
<td><p><span data-ttu-id="186f9-115">現在の行セットのスキーマを表します。</span><span class="sxs-lookup"><span data-stu-id="186f9-115">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="186f9-p101">仕様に定義されているように、クライアントは独自のタグをこれらの名前空間に追加することはできません。たとえば、クライアントは名前空間を "urn:schemas-microsoft-com:rowset" として定義し、"rs:MyOwnTag" などを書き込むことはできません。名前空間の詳細については、「[XML 名前空間 (英語)](https://www.w3.org/tr/xml-names/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="186f9-p101">A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="186f9-119">[!メモ] スキーマ タグの ID は "RowsetSchema" であることが必要です。また、現在の行セットのスキーマを表すために使用される名前空間は、"#RowsetSchema" を指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="186f9-119">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="186f9-120">名前空間のプレフィックス (コロンの右側で等号の左側の部分) は任意です。</span><span class="sxs-lookup"><span data-stu-id="186f9-120">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="186f9-p102">この名前が XML ドキュメント全体で一貫して使用される限り、ユーザーはこれを任意の名前に定義できます。ADO は常に "s"、"rs"、"dt"、および "z" を書き込みますが、これらのプレフィックス名は、読み込むコンポーネント内にはハードコーディングされません。</span><span class="sxs-lookup"><span data-stu-id="186f9-p102">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

## <a name="namespaces"></a><span data-ttu-id="186f9-123">名前空間</span><span class="sxs-lookup"><span data-stu-id="186f9-123">Namespaces</span></span>

<span data-ttu-id="186f9-124">ADO での XML の保存形式には、次の 4 つの名前空間が使用されます。</span><span class="sxs-lookup"><span data-stu-id="186f9-124">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="186f9-125">接頭語</span><span class="sxs-lookup"><span data-stu-id="186f9-125">Prefix</span></span></p></th>
<th><p><span data-ttu-id="186f9-126">説明</span><span class="sxs-lookup"><span data-stu-id="186f9-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="186f9-127">s</span><span class="sxs-lookup"><span data-stu-id="186f9-127">s</span></span></p></td>
<td><p><span data-ttu-id="186f9-128">参照して、 &quot;XML データ&quot;名前空間の要素と現在の<strong>レコード セット</strong>のスキーマを定義する属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="186f9-128">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186f9-129">dt</span><span class="sxs-lookup"><span data-stu-id="186f9-129">dt</span></span></p></td>
<td><p><span data-ttu-id="186f9-130">データ型定義の仕様を表します。</span><span class="sxs-lookup"><span data-stu-id="186f9-130">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="186f9-131">rs</span><span class="sxs-lookup"><span data-stu-id="186f9-131">rs</span></span></p></td>
<td><p><span data-ttu-id="186f9-132">ADO の <strong>Recordset</strong> プロパティおよび属性に固有の要素と属性を含む名前空間を表します。</span><span class="sxs-lookup"><span data-stu-id="186f9-132">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186f9-133">z</span><span class="sxs-lookup"><span data-stu-id="186f9-133">z</span></span></p></td>
<td><p><span data-ttu-id="186f9-134">現在の行セットのスキーマを表します。</span><span class="sxs-lookup"><span data-stu-id="186f9-134">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="186f9-p103">仕様に定義されているように、クライアントは独自のタグをこれらの名前空間に追加することはできません。たとえば、クライアントは名前空間を "urn:schemas-microsoft-com:rowset" として定義し、"rs:MyOwnTag" などを書き込むことはできません。名前空間の詳細については、「[XML 名前空間 (英語)](https://www.w3.org/tr/xml-names/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="186f9-p103">A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="186f9-138">[!メモ] スキーマ タグの ID は "RowsetSchema" であることが必要です。また、現在の行セットのスキーマを表すために使用される名前空間は、"#RowsetSchema" を指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="186f9-138">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="186f9-139">名前空間のプレフィックス (コロンの右側で等号の左側の部分) は任意です。</span><span class="sxs-lookup"><span data-stu-id="186f9-139">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="186f9-p104">この名前が XML ドキュメント全体で一貫して使用される限り、ユーザーはこれを任意の名前に定義できます。ADO は常に "s"、"rs"、"dt"、および "z" を書き込みますが、これらのプレフィックス名は、読み込むコンポーネント内にはハードコーディングされません。</span><span class="sxs-lookup"><span data-stu-id="186f9-p104">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

