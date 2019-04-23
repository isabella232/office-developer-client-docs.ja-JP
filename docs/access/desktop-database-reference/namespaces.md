---
title: 名前空間 (Access デスクトップデータベースリファレンス)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288626"
---
# <a name="namespaces"></a><span data-ttu-id="f7bba-102">名前空間</span><span class="sxs-lookup"><span data-stu-id="f7bba-102">Namespaces</span></span>

<span data-ttu-id="f7bba-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7bba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7bba-104">ADO での XML の保存形式には、次の 4 つの名前空間が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7bba-104">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7bba-105">Prefix</span><span class="sxs-lookup"><span data-stu-id="f7bba-105">Prefix</span></span></p></th>
<th><p><span data-ttu-id="f7bba-106">説明</span><span class="sxs-lookup"><span data-stu-id="f7bba-106">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7bba-107">s</span><span class="sxs-lookup"><span data-stu-id="f7bba-107">s</span></span></p></td>
<td><p><span data-ttu-id="f7bba-108">現在の<strong>Recordset</strong>のスキーマを&quot;定義する要素と属性を含む&quot;XML データ名前空間を参照します。</span><span class="sxs-lookup"><span data-stu-id="f7bba-108">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7bba-109">dt</span><span class="sxs-lookup"><span data-stu-id="f7bba-109">dt</span></span></p></td>
<td><p><span data-ttu-id="f7bba-110">データ型定義の仕様を表します。</span><span class="sxs-lookup"><span data-stu-id="f7bba-110">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7bba-111">clr</span><span class="sxs-lookup"><span data-stu-id="f7bba-111">rs</span></span></p></td>
<td><p><span data-ttu-id="f7bba-112">ADO の <strong>Recordset</strong> プロパティおよび属性に固有の要素と属性を含む名前空間を表します。</span><span class="sxs-lookup"><span data-stu-id="f7bba-112">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7bba-113">z</span><span class="sxs-lookup"><span data-stu-id="f7bba-113">z</span></span></p></td>
<td><p><span data-ttu-id="f7bba-114">現在の行セットのスキーマを表します。</span><span class="sxs-lookup"><span data-stu-id="f7bba-114">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f7bba-p101">仕様に定義されているように、クライアントは独自のタグをこれらの名前空間に追加することはできません。たとえば、クライアントは名前空間を "urn:schemas-microsoft-com:rowset" として定義し、"rs:MyOwnTag" などを書き込むことはできません。名前空間の詳細については、「[XML 名前空間 (英語)](https://www.w3.org/tr/xml-names/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7bba-p101">A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>

> [!NOTE]
> <span data-ttu-id="f7bba-118">[!メモ] スキーマ タグの ID は "RowsetSchema" であることが必要です。また、現在の行セットのスキーマを表すために使用される名前空間は、"#RowsetSchema" を指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7bba-118">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span>

<span data-ttu-id="f7bba-119">名前空間のプレフィックス (コロンの右側で等号の左側の部分) は任意です。</span><span class="sxs-lookup"><span data-stu-id="f7bba-119">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="f7bba-p102">この名前が XML ドキュメント全体で一貫して使用される限り、ユーザーはこれを任意の名前に定義できます。ADO は常に "s"、"rs"、"dt"、および "z" を書き込みますが、これらのプレフィックス名は、読み込むコンポーネント内にはハードコーディングされません。</span><span class="sxs-lookup"><span data-stu-id="f7bba-p102">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>



