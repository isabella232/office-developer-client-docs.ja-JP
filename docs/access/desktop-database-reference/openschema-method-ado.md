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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288337"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="7f493-102">OpenSchema メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f493-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="7f493-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f493-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f493-104">プロバイダーからデータベースのスキーマ情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f493-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="7f493-105">構文</span><span class="sxs-lookup"><span data-stu-id="7f493-105">Syntax</span></span>

<span data-ttu-id="7f493-106">**Set \* \* \* recordset* = *接続*。OpenSchema (* QueryType \*、 *Criteria*、 *schemaid*)</span><span class="sxs-lookup"><span data-stu-id="7f493-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="7f493-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="7f493-107">Return values</span></span>

<span data-ttu-id="7f493-108">スキーマ情報を含む [Recordset](recordset-object-ado.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7f493-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="7f493-109">**Recordset** は読み取り専用の静的カーソルとして開かれます。</span><span class="sxs-lookup"><span data-stu-id="7f493-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="7f493-110">*QueryType* により、**Recordset** に表示される列が決まります。</span><span class="sxs-lookup"><span data-stu-id="7f493-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f493-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7f493-111">Parameters</span></span>

|<span data-ttu-id="7f493-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7f493-112">Parameter</span></span>|<span data-ttu-id="7f493-113">説明</span><span class="sxs-lookup"><span data-stu-id="7f493-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7f493-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="7f493-114">*QueryType*</span></span> |<span data-ttu-id="7f493-115">実行するスキーマ クエリの種類を表す [SchemaEnum](schemaenum.md) 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f493-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="7f493-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="7f493-116">*Criteria*</span></span> |<span data-ttu-id="7f493-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7f493-117">Optional.</span></span> <span data-ttu-id="7f493-118">**SchemaEnum** の指定に従って、各 *QueryType* オプションのクエリ制約の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f493-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="7f493-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="7f493-119">*SchemaID*</span></span> |<span data-ttu-id="7f493-p103">OLE DB の仕様で定義されていない、プロバイダー スキーマのクエリの GUID (グローバル一意識別子) を指定します。このパラメーターは、*QueryType* が **adSchemaProviderSpecific** に設定されている場合は必須です。それ以外の場合、このパラメーターは使用しません。</span><span class="sxs-lookup"><span data-stu-id="7f493-p103">The GUID for a provider-schema query not defined by the OLE DB specification. This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7f493-122">注釈</span><span class="sxs-lookup"><span data-stu-id="7f493-122">Remarks</span></span>

<span data-ttu-id="7f493-123">**OpenSchema** メソッドは、データ ソースに含まれるテーブル、テーブルに含まれる列、サポートされているデータ型などのデータ ソースに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="7f493-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="7f493-p104">*QueryType* 引数は、返される列 (スキーマ) を示す GUID です。OLE DB の仕様には、すべてのスキーマの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="7f493-p104">The *QueryType* argument is a GUID that indicates the columns (schemas) returned. The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="7f493-126">引数*Criteria*は、スキーマクエリの結果を制限します。</span><span class="sxs-lookup"><span data-stu-id="7f493-126">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="7f493-127">*Criteria*には、結果の**Recordset**で、対応する列の列のサブセット (*制約列*) に必要な値の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f493-127">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="7f493-p106">OLE DB 仕様以外の非標準スキーマ クエリをプロバイダーが独自に定義している場合は、*QueryType* 引数に **adSchemaProviderSpecific** を使用します。この定数を使用する場合は、*SchemaID* 引数に、実行するスキーマ クエリの GUID を指定する必要があります。*QueryType* が **adSchemaProviderSpecific** に設定され、*SchemaID* が指定されていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7f493-p106">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above. When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute. If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="7f493-p107">プロバイダーは、すべての OLE DB 標準スキーマ クエリをサポートする必要はありません。OLE DB の仕様では、**adSchemaTables**、**adSchemaColumns**、および **adSchemaProviderTypes** のみが必要とされます。ただし、これらのスキーマ クエリでは、プロバイダーは *Criteria* の制約をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7f493-p107">Providers are not required to support all of the OLE DB standard schema queries. Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification. However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="7f493-134">**リモートデータサービスの使用状況\*\*\*\*OpenSchema**メソッドは、クライアント側の[Connection](connection-object-ado.md)オブジェクトでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7f493-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="7f493-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables.</span><span class="sxs-lookup"><span data-stu-id="7f493-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables.</span></span> <span data-ttu-id="7f493-136">ole db データ型の詳細については、「 *Microsoft ole db プログラマリファレンス*」の「第13章」および「付録 a」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f493-136">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


