---
title: Query メソッド (RDS-Access デスクトップデータベースリファレンス)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301114"
---
# <a name="query-method-rds"></a><span data-ttu-id="0f30b-102">Query メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="0f30b-102">Query method (RDS)</span></span>

<span data-ttu-id="0f30b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f30b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f30b-104">有効な SQL クエリ文字列を使用して [Recordset](recordset-object-ado.md) を返します。</span><span class="sxs-lookup"><span data-stu-id="0f30b-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f30b-105">構文</span><span class="sxs-lookup"><span data-stu-id="0f30b-105">Syntax</span></span>

<span data-ttu-id="0f30b-106">*Recordset* = *DataFactory*を設定します。クエリ (*接続*、*クエリ*)</span><span class="sxs-lookup"><span data-stu-id="0f30b-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="0f30b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f30b-107">Parameters</span></span>

|<span data-ttu-id="0f30b-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f30b-108">Parameter</span></span>|<span data-ttu-id="0f30b-109">説明</span><span class="sxs-lookup"><span data-stu-id="0f30b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0f30b-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="0f30b-110">*Recordset*</span></span> |<span data-ttu-id="0f30b-111">**Recordset** オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f30b-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="0f30b-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="0f30b-112">*DataFactory*</span></span> |<span data-ttu-id="0f30b-113">[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数。</span><span class="sxs-lookup"><span data-stu-id="0f30b-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="0f30b-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="0f30b-114">*Connection*</span></span> |<span data-ttu-id="0f30b-p101">サーバー接続情報を含む文字列型 ( **String** ) の値を指定します。このパラメーターは [Connect](connect-property-rds.md) プロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="0f30b-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="0f30b-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="0f30b-117">*Query*</span></span> |<span data-ttu-id="0f30b-118">SQL クエリを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f30b-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0f30b-119">注釈</span><span class="sxs-lookup"><span data-stu-id="0f30b-119">Remarks</span></span>

<span data-ttu-id="0f30b-p102">クエリでは、データベース サーバーの SQL 文法を使用する必要があります。実行したクエリにエラーがある場合は、結果のステータスが返されます。**Query** メソッドでは、**Query** 文字列の構文チェックは行われません。</span><span class="sxs-lookup"><span data-stu-id="0f30b-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

