---
title: Workspace.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6427b99fd212fa358b70fb20a5ecf0c9180209fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476255"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="ea4b8-102">Workspace.LoginTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ea4b8-102">Workspace.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="ea4b8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea4b8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ea4b8-104">ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ea4b8-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4b8-105">構文</span><span class="sxs-lookup"><span data-stu-id="ea4b8-105">Syntax</span></span>

<span data-ttu-id="ea4b8-106">*式*です。LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="ea4b8-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="ea4b8-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ea4b8-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4b8-108">注釈</span><span class="sxs-lookup"><span data-stu-id="ea4b8-108">Remarks</span></span>

<span data-ttu-id="ea4b8-p101">**LoginTimeout** プロパティの既定の設定は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。</span><span class="sxs-lookup"><span data-stu-id="ea4b8-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="ea4b8-p102">Microsoft SQL Server などの ODBC データベースへのログオンを試みたときに、ネットワーク エラーが発生したりサーバーが実行中でないことが原因で、接続に失敗したりする場合があります。接続時に既定の 20 秒間待機する代わりに、エラーが発生するまでの時間を指定できます。外部のサーバー データベースに対するクエリの実行など、多くのさまざまなイベントの一部として、サーバーへの暗黙的なログオンが発生します。</span><span class="sxs-lookup"><span data-stu-id="ea4b8-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

