---
title: DBEngine.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e3ff893a16e650fe7eb49b647ae8d67374375a0d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701929"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="1ab2b-102">DBEngine.LoginTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ab2b-102">DBEngine.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="1ab2b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1ab2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ab2b-104">ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="1ab2b-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab2b-105">構文</span><span class="sxs-lookup"><span data-stu-id="1ab2b-105">Syntax</span></span>

<span data-ttu-id="1ab2b-106">*式*です。LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="1ab2b-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="1ab2b-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="1ab2b-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ab2b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="1ab2b-108">Remarks</span></span>

<span data-ttu-id="1ab2b-p101">**LoginTimeout** プロパティの既定の設定は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。</span><span class="sxs-lookup"><span data-stu-id="1ab2b-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="1ab2b-p102">Microsoft SQL Server などの ODBC データベースへのログオンを試みたときに、ネットワーク エラーが発生したりサーバーが実行中でないことが原因で、接続に失敗したりする場合があります。接続時に既定の 20 秒間待機する代わりに、エラーが発生するまでの時間を指定できます。外部のサーバー データベースに対するクエリの実行など、多くのさまざまなイベントの一部として、サーバーへの暗黙的なログオンが発生します。</span><span class="sxs-lookup"><span data-stu-id="1ab2b-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

