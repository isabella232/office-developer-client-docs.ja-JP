---
title: CopyDatabaseFile マクロ アクション
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3c98d8795bb7039c0ae158414401dc5d754066f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295500"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="8b8ad-102">CopyDatabaseFile マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="8b8ad-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="8b8ad-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b8ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b8ad-104">" **CopyDatabaseFile/データベースファイルのコピー** " アクションを使用すると、Access プロジェクトに接続されている Microsoft SQL Server 7.0 以降のカレント データベースのコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="8b8ad-105">Access は、現在のデータベースをデタッチして、そのデータベースを転送先サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="8b8ad-106">データベースの切断と接続の詳細については、SQL Server のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="8b8ad-107">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="8b8ad-108">設定値</span><span class="sxs-lookup"><span data-stu-id="8b8ad-108">Setting</span></span>

<span data-ttu-id="8b8ad-109">"CopyDatabaseFile/データベースファイルのコピー" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b8ad-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="8b8ad-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8b8ad-111">説明</span><span class="sxs-lookup"><span data-stu-id="8b8ad-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b8ad-112"><strong>Database File Name/データベース ファイル名</strong></span><span class="sxs-lookup"><span data-stu-id="8b8ad-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8b8ad-p102">新しいマスター データ ファイルの名前を指定します。このファイルの既定のパスは、Access プロジェクト ファイル (.adp) の現在の場所です。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-p102">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b8ad-115"><strong>Overwrite Existing File/既存ファイルの上書き</strong></span><span class="sxs-lookup"><span data-stu-id="8b8ad-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="8b8ad-p103">既存のファイルを同じ名前のファイルで置き換えるかどうかを指定します。[はい] に設定した場合に、同じ名前のファイルが既に存在すると、ファイルは上書きされます。[いいえ] に設定した場合、同じ名前のファイルが既に存在すると、ファイルは上書きされず、アクションは失敗します。同じ名前のファイルが存在しない場合、この設定は無視されます。既定値は [はい] です。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-p103">Specifies whether or not to replace an existing file with the same name. If set to <strong>Yes</strong> and the filename already exists, the file is overwritten. If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails. If the file does not already exist, this setting is ignored. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b8ad-121"><strong>Disconnect All Users/全ユーザーの切断</strong></span><span class="sxs-lookup"><span data-stu-id="8b8ad-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="8b8ad-122">ユーザーを強制的にデータベースから切断するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-122">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="8b8ad-123">[はい] に設定した場合は、カレント データベースに接続されているすべてのユーザーを切断し、データベースのコピー操作を進めることができます。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-123">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="8b8ad-124">[いいえ] に設定した場合は、データベースに接続しているユーザーが 1 人でもいると、データベースのコピー操作は失敗します。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-124">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="8b8ad-125">既定値は [いいえ] です。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-125">The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="8b8ad-126"><strong>警告</strong>: 適切な警告なしにデータベースからユーザーを切断すると、データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8b8ad-127">注釈</span><span class="sxs-lookup"><span data-stu-id="8b8ad-127">Remarks</span></span>

<span data-ttu-id="8b8ad-128">コピー操作は同期操作であるため、データベースのコピーが完了するまで他の操作は実行できません。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="8b8ad-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span><span class="sxs-lookup"><span data-stu-id="8b8ad-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="8b8ad-130">データベースのコピー操作の要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="8b8ad-131">データベース ファイルをコピーする前にすべてのアプリケーションとユーザーを切断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="8b8ad-132">ナビゲーション ウィンドウ以外のすべてのオブジェクトとビューを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="8b8ad-133">カレント データベースはレプリケートできません。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="8b8ad-134">サーバー データベースをコピーするには、ローカル コンピューターに Microsoft SQL Server Version 7.0 以降または SQL Server 2000 Desktop Engine が必要です。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="8b8ad-135">コピー元のサーバーにある SQL Server データベースは、単一のファイル データベースであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="8b8ad-136">コピーを実行するユーザーは、コピー元とコピー先の両方の SQL Server コンピューターにおいて sysadmin ロールのメンバーである必要がありです。</span><span class="sxs-lookup"><span data-stu-id="8b8ad-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="8b8ad-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="8b8ad-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

