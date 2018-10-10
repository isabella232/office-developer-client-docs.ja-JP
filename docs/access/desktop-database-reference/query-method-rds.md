---
title: Query メソッド (RDS のデスクトップのデータベース参照のアクセス)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a9ecb2d7ebfdd8f6738b8d7b9b8738ce981ec16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476676"
---
# <a name="query-method-rds"></a><span data-ttu-id="b1fdf-102">Query メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="b1fdf-102">Query Method (RDS)</span></span>


<span data-ttu-id="b1fdf-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1fdf-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="b1fdf-104">有効な SQL クエリ文字列を使用して [Recordset](recordset-object-ado.md) を返します。</span><span class="sxs-lookup"><span data-stu-id="b1fdf-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1fdf-105">構文</span><span class="sxs-lookup"><span data-stu-id="b1fdf-105">Syntax</span></span>

<span data-ttu-id="b1fdf-106">*レコード セット*を設定する = *DataFactory*。クエリ (*接続*、*クエリ*)</span><span class="sxs-lookup"><span data-stu-id="b1fdf-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="b1fdf-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1fdf-107">Parameters</span></span>

  - <span data-ttu-id="b1fdf-108">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="b1fdf-108">*Recordset*</span></span>

  - <span data-ttu-id="b1fdf-109">**Recordset** オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1fdf-109">An object variable that represents a **Recordset** object.</span></span>

  - <span data-ttu-id="b1fdf-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="b1fdf-110">*DataFactory*</span></span>

  - <span data-ttu-id="b1fdf-111">[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1fdf-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="b1fdf-112">*Connection*</span><span class="sxs-lookup"><span data-stu-id="b1fdf-112">*Connection*</span></span>

  - <span data-ttu-id="b1fdf-p101">サーバー接続情報を含む文字列型 ( **String** ) の値を指定します。このパラメーターは [Connect](connect-property-rds.md) プロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="b1fdf-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>

  - <span data-ttu-id="b1fdf-115">*Query*</span><span class="sxs-lookup"><span data-stu-id="b1fdf-115">*Query*</span></span>

  - <span data-ttu-id="b1fdf-116">SQL クエリを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1fdf-116">A **String** that contains the SQL query.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1fdf-117">解説</span><span class="sxs-lookup"><span data-stu-id="b1fdf-117">Remarks</span></span>

<span data-ttu-id="b1fdf-p102">クエリでは、データベース サーバーの SQL 文法を使用する必要があります。実行したクエリにエラーがある場合は、結果のステータスが返されます。 **Query** メソッドでは、 **Query** 文字列の構文チェックは行われません。</span><span class="sxs-lookup"><span data-stu-id="b1fdf-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

