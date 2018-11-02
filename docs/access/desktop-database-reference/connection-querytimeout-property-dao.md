---
title: Connection.QueryTimeout プロパティ (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c096ba38c59ec9c62da56dc47a59f06254ef60f6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921741"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="331bc-102">Connection.QueryTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="331bc-102">Connection.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="331bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="331bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="331bc-104">ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="331bc-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="331bc-105">構文</span><span class="sxs-lookup"><span data-stu-id="331bc-105">Syntax</span></span>

<span data-ttu-id="331bc-106">*式*です。QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="331bc-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="331bc-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="331bc-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="331bc-108">注釈</span><span class="sxs-lookup"><span data-stu-id="331bc-108">Remarks</span></span>

<span data-ttu-id="331bc-109">既定値は 60 です。</span><span class="sxs-lookup"><span data-stu-id="331bc-109">The default value is 60.</span></span>

<span data-ttu-id="331bc-p101">Microsoft SQL Server などの ODBC データベースを使用している場合、ネットワーク トラフィックや ODBC サーバーに対する負荷の増大のために、応答が遅れることがあります。無限に待機せずに、待機する時間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="331bc-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="331bc-p102">[**Connection**](connection-object-dao.md) オブジェクトまたは [**Database**](database-object-dao.md) オブジェクトで **QueryTimeout** プロパティを使用する場合、データベースに関連付けられているすべてのクエリに対してグローバル値を指定します。特定の [**QueryDef**](querydef-object-dao.md) オブジェクトの **ODBCTimeout** プロパティを設定すると、特定のクエリに対してこのグローバル値より優先させることができます。</span><span class="sxs-lookup"><span data-stu-id="331bc-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

