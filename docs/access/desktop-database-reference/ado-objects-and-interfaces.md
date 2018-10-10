---
title: ADO オブジェクトとインターフェイス
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ce04896e6ae59af6917497d9e37dc1ae97222eff
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476557"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="58203-102">ADO オブジェクトとインターフェイス</span><span class="sxs-lookup"><span data-stu-id="58203-102">ADO Objects and Interfaces</span></span>


<span data-ttu-id="58203-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="58203-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="58203-104">これらのオブジェクトの関係については、ADO オブジェクト モデルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58203-104">The relationships between these objects are represented in the ADO Object Model.</span></span>

<span data-ttu-id="58203-p101">各オブジェクトは、対応するコレクションに格納できます。たとえば、[Error](error-object-ado.md) オブジェクトは [Errors](errors-collection-ado.md) コレクションに格納できます。詳細については、「 [ADO コレクション](ado-collections.md)」、またはコレクションの特定の項目を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58203-p101">Each object can be contained in its corresponding collection. For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection. For more information, see [ADO Collections](ado-collections.md) or a specific collection topic.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58203-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="58203-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="58203-109">C/C++ アプリケーションで OLE DB <strong>Row</strong> オブジェクトから ADO <strong>Record</strong> オブジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="58203-109">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58203-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="58203-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="58203-111">C/C++ アプリケーションで OLE DB <strong>Rowset</strong> オブジェクトから ADO <strong>Recordset</strong> オブジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="58203-111">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58203-112"><a href="error-object-ado.md">エラー</a></span><span class="sxs-lookup"><span data-stu-id="58203-112"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="58203-113">プロバイダーを含む単一の操作に関連して発生した、データ アクセス エラーの詳細情報を格納しています。</span><span class="sxs-lookup"><span data-stu-id="58203-113">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58203-114"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="58203-114"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="58203-115">共通のデータ型を持つデータの列を表します。</span><span class="sxs-lookup"><span data-stu-id="58203-115">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58203-116"><a href="parameter-object-ado.md">パラメーター</a></span><span class="sxs-lookup"><span data-stu-id="58203-116"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="58203-117">パラメーター クエリまたはストアド プロシージャに基づく、<strong>Command</strong> オブジェクトに関連付けられたパラメーターまたは引数を表します。</span><span class="sxs-lookup"><span data-stu-id="58203-117">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58203-118"><a href="property-object-ado.md">プロパティ</a></span><span class="sxs-lookup"><span data-stu-id="58203-118"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="58203-119">プロバイダーで定義される ADO オブジェクトの動的特性を表します。</span><span class="sxs-lookup"><span data-stu-id="58203-119">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58203-120"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="58203-120"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="58203-121"><strong>Recordset</strong> の行、またはファイル システム内のディレクトリやファイルを表します。</span><span class="sxs-lookup"><span data-stu-id="58203-121">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58203-122"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="58203-122"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="58203-p102">基になるテーブルのレコードセット全体、またはコマンドの実行によって返された結果を表します。 <strong>Recordset</strong> オブジェクトでは、常にレコードセット内の 1 つのレコードのみをカレント レコードとして参照します。</span><span class="sxs-lookup"><span data-stu-id="58203-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58203-125"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="58203-125"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="58203-126">データのバイナリ ストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="58203-126">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

