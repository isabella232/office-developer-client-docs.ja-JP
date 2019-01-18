---
title: OpenSchema メソッド (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701012"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="590e1-102">OpenSchema メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="590e1-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="590e1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="590e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="590e1-104">プロバイダーからデータベースのスキーマ情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="590e1-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="590e1-105">構文</span><span class="sxs-lookup"><span data-stu-id="590e1-105">Syntax</span></span>

<span data-ttu-id="590e1-106">**設定。 レコード セット* = *接続*します。OpenSchema (* QueryType *、*条件\*、 *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="590e1-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="590e1-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="590e1-107">Return values</span></span>

<span data-ttu-id="590e1-108">スキーマ情報を含む [Recordset](recordset-object-ado.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="590e1-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="590e1-109">**Recordset** は読み取り専用の静的カーソルとして開かれます。</span><span class="sxs-lookup"><span data-stu-id="590e1-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="590e1-110">*QueryType*は、**レコード セット**に表示する列を決定します。</span><span class="sxs-lookup"><span data-stu-id="590e1-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="590e1-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="590e1-111">Parameters</span></span>

|<span data-ttu-id="590e1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="590e1-112">Parameter</span></span>|<span data-ttu-id="590e1-113">説明</span><span class="sxs-lookup"><span data-stu-id="590e1-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="590e1-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="590e1-114">*QueryType*</span></span> |<span data-ttu-id="590e1-115">実行するスキーマ クエリの種類を表す [SchemaEnum](schemaenum.md) 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="590e1-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="590e1-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="590e1-116">*Criteria*</span></span> |<span data-ttu-id="590e1-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="590e1-117">Optional.</span></span> <span data-ttu-id="590e1-118">**SchemaEnum**に記載されている各*QueryType*オプション、クエリの制約の配列。</span><span class="sxs-lookup"><span data-stu-id="590e1-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="590e1-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="590e1-119">*SchemaID*</span></span> |<span data-ttu-id="590e1-120">OLE DB 仕様で定義されていないプロバイダー スキーマ クエリの GUID です。</span><span class="sxs-lookup"><span data-stu-id="590e1-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="590e1-121">*QueryType*が**adSchemaProviderSpecific**; に設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="590e1-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="590e1-122">解説</span><span class="sxs-lookup"><span data-stu-id="590e1-122">Remarks</span></span>

<span data-ttu-id="590e1-123">**OpenSchema** メソッドは、データ ソースに含まれるテーブル、テーブルに含まれる列、サポートされているデータ型などのデータ ソースに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="590e1-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="590e1-124">*QueryType*引数は、列 (スキーマ) が返されるかを示す GUID です。</span><span class="sxs-lookup"><span data-stu-id="590e1-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="590e1-125">OLE DB の仕様には、すべてのスキーマの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="590e1-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="590e1-126">引数*Criteria*は、スキーマ クエリの結果を制限します。</span><span class="sxs-lookup"><span data-stu-id="590e1-126">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="590e1-127">*条件*では、列、*制約の列*、結果の**レコード セット**内の対応するサブセットで行う必要のある値の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="590e1-127">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="590e1-128">プロバイダーが上記以外の独自の非標準スキーマ クエリを定義する場合は、 *QueryType*引数の定数**adSchemaProviderSpecific**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="590e1-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="590e1-129">この定数を使用する場合に実行するスキーマ クエリの GUID を渡す、 *SchemaID*引数が必要です。</span><span class="sxs-lookup"><span data-stu-id="590e1-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="590e1-130">*QueryType*が**adSchemaProviderSpecific**に設定されて場合は、 *SchemaID*が指定されていないエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="590e1-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="590e1-131">プロバイダーは、すべての OLE DB 標準スキーマ クエリをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="590e1-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="590e1-132">OLE DB の仕様では、 **adSchemaTables** 、 **adSchemaColumns** 、および **adSchemaProviderTypes** のみが必要とされます。</span><span class="sxs-lookup"><span data-stu-id="590e1-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="590e1-133">ただし、プロバイダーは*Criteria*の制約上これらのスキーマ クエリをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="590e1-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="590e1-134">**リモート データ サービスの使用法\*\*\*\*OpenSchema**メソッドがクライアント側の[Connection](connection-object-ado.md)オブジェクトで使用可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="590e1-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="590e1-135">Visual Basic では、 **Connection**オブジェクトの**OpenSchema**メソッドから返される**レコード セット**では 4 バイトの符号なし整数 (DBTYPE UI4) が設定されている列は他の変数を比較できません。</span><span class="sxs-lookup"><span data-stu-id="590e1-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables.</span></span> <span data-ttu-id="590e1-136">OLE DB データ型の詳細については、第 13 章と付録 A の*Microsoft OLE DB プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="590e1-136">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


