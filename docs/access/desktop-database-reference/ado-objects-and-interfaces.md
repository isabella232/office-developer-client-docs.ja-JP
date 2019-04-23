---
title: ADO のオブジェクトとインターフェイス
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 539feb1918877189548d0e7cff6ceb28e50abddc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283262"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="c2af5-102">ADO のオブジェクトとインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c2af5-102">ADO objects and interfaces</span></span>

<span data-ttu-id="c2af5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2af5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2af5-104">これらのオブジェクト間のリレーションシップは、ActiveX Data objects (ADO) オブジェクトモデルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c2af5-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="c2af5-105">各オブジェクトは、対応するコレクションに格納できます。</span><span class="sxs-lookup"><span data-stu-id="c2af5-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="c2af5-106">たとえば、[Error](error-object-ado.md) オブジェクトは [Errors](errors-collection-ado.md) コレクションに格納できます。</span><span class="sxs-lookup"><span data-stu-id="c2af5-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="c2af5-107">詳細については、「 [ADO コレクション](ado-collections.md)」または「特定のコレクションのトピック」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2af5-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="c2af5-108">Object</span><span class="sxs-lookup"><span data-stu-id="c2af5-108">Object</span></span></th>
<th><span data-ttu-id="c2af5-109">説明</span><span class="sxs-lookup"><span data-stu-id="c2af5-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2af5-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-111">C/C++ アプリケーションで OLE DB <strong>Row</strong> オブジェクトから ADO <strong>Record</strong> オブジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2af5-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-113">C/C++ アプリケーションで OLE DB <strong>Rowset</strong> オブジェクトから ADO <strong>Recordset</strong> オブジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2af5-114"><a href="error-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-115">データ ソースに対して実行する特定のコマンドを定義します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2af5-116"><a href="field-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-117">データ ソースに対して開かれている接続を表します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2af5-118"><a href="error-object-ado.md">Error</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-119">プロバイダーを含む単一の操作に関連して発生した、データ アクセス エラーの詳細情報を格納しています。</span><span class="sxs-lookup"><span data-stu-id="c2af5-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2af5-120"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-121">共通のデータ型を持つデータの列を表します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2af5-122"><a href="parameter-object-ado.md">パラメーター</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-123">パラメーター クエリまたはストアド プロシージャに基づく、<strong>Command</strong> オブジェクトに関連付けられたパラメーターまたは引数を表します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2af5-124"><a href="property-object-ado.md">Property</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-125">プロバイダーで定義される ADO オブジェクトの動的特性を表します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2af5-126"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-127"><strong>Recordset</strong> の行、またはファイル システム内のディレクトリやファイルを表します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2af5-128"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-p102">基になるテーブルのレコードセット全体、またはコマンドの実行によって返された結果を表します。 <strong>Recordset</strong> オブジェクトでは、常にレコードセット内の 1 つのレコードのみをカレント レコードとして参照します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2af5-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="c2af5-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="c2af5-132">データのバイナリ ストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="c2af5-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

