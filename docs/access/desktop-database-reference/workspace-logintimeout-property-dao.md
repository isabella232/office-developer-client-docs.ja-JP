---
title: Workspace.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07b2945f2e9a59cc8a7db4a6f5a44cfaf9b35043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928286"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="3c9ba-102">Workspace.LoginTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c9ba-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="3c9ba-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3c9ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c9ba-104">ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="3c9ba-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9ba-105">構文</span><span class="sxs-lookup"><span data-stu-id="3c9ba-105">Syntax</span></span>

<span data-ttu-id="3c9ba-106">*式*です。LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="3c9ba-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="3c9ba-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="3c9ba-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c9ba-108">注釈</span><span class="sxs-lookup"><span data-stu-id="3c9ba-108">Remarks</span></span>

<span data-ttu-id="3c9ba-p101">**LoginTimeout** プロパティの既定の設定は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。</span><span class="sxs-lookup"><span data-stu-id="3c9ba-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="3c9ba-p102">Microsoft SQL Server などの ODBC データベースへのログオンを試みたときに、ネットワーク エラーが発生したりサーバーが実行中でないことが原因で、接続に失敗したりする場合があります。接続時に既定の 20 秒間待機する代わりに、エラーが発生するまでの時間を指定できます。外部のサーバー データベースに対するクエリの実行など、多くのさまざまなイベントの一部として、サーバーへの暗黙的なログオンが発生します。</span><span class="sxs-lookup"><span data-stu-id="3c9ba-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

