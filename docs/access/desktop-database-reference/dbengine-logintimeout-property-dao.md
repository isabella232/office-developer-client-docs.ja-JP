---
title: DBEngine タイムアウトプロパティ (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294310"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="59d83-102">DBEngine タイムアウトプロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="59d83-102">DBEngine.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="59d83-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="59d83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59d83-104">ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="59d83-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d83-105">構文</span><span class="sxs-lookup"><span data-stu-id="59d83-105">Syntax</span></span>

<span data-ttu-id="59d83-106">*式*。LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="59d83-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="59d83-107">\*式\***DBEngine**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="59d83-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d83-108">注釈</span><span class="sxs-lookup"><span data-stu-id="59d83-108">Remarks</span></span>

<span data-ttu-id="59d83-p101">**LoginTimeout** プロパティの既定の設定値は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。</span><span class="sxs-lookup"><span data-stu-id="59d83-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="59d83-p102">Microsoft SQL Server などの ODBC データベースにログオンしようとすると、ネットワーク エラーが発生するか、サーバーが動作していないために、接続が失敗する可能性があります。既定の 20 秒間待機してから接続するのではなく、待機する時間を指定し、それを超えたらエラーとすることができます。サーバーへのログオンは、外部サーバー データベースでのクエリの実行など、多数の異なるイベントの一環として暗黙に実行されます。</span><span class="sxs-lookup"><span data-stu-id="59d83-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

