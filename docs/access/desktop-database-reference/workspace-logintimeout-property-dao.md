---
title: Workspace タイムアウトプロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306910"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="67f37-102">Workspace タイムアウトプロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="67f37-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="67f37-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="67f37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67f37-104">ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="67f37-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f37-105">構文</span><span class="sxs-lookup"><span data-stu-id="67f37-105">Syntax</span></span>

<span data-ttu-id="67f37-106">*式*。LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="67f37-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="67f37-107">\*式\***Workspace**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="67f37-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f37-108">注釈</span><span class="sxs-lookup"><span data-stu-id="67f37-108">Remarks</span></span>

<span data-ttu-id="67f37-p101">**LoginTimeout** プロパティの既定の設定値は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。</span><span class="sxs-lookup"><span data-stu-id="67f37-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="67f37-p102">Microsoft SQL Server などの ODBC データベースにログオンしようとすると、ネットワーク エラーが発生するか、サーバーが動作していないために、接続が失敗する可能性があります。既定の 20 秒間待機してから接続するのではなく、待機する時間を指定し、それを超えたらエラーとすることができます。サーバーへのログオンは、外部サーバー データベースでのクエリの実行など、多数の異なるイベントの一環として暗黙に実行されます。</span><span class="sxs-lookup"><span data-stu-id="67f37-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

