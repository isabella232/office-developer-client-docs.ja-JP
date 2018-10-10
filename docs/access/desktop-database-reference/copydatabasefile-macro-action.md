---
title: "\"CopyDatabaseFile/データベースファイルのコピー\" マクロ アクション"
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b52644cb9a0a5140f45c42eaead84a63723c23e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479176"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="8d570-102">"CopyDatabaseFile/データベースファイルのコピー" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="8d570-102">CopyDatabaseFile Macro Action</span></span>


<span data-ttu-id="8d570-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d570-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d570-104">" **CopyDatabaseFile/データベースファイルのコピー** " アクションを使用すると、Access プロジェクトに接続されている Microsoft SQL Server 7.0 以降のカレント データベースのコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8d570-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="8d570-105">アクセスでは、現在のデータベースをデタッチし、移行先サーバーに結び付けます。</span><span class="sxs-lookup"><span data-stu-id="8d570-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="8d570-106">データベースの切断と接続の詳細については、SQL Server のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d570-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d570-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d570-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="8d570-109">設定値</span><span class="sxs-lookup"><span data-stu-id="8d570-109">Setting</span></span>

<span data-ttu-id="8d570-110">**データベースファイルのコピー**操作では、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="8d570-110">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d570-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="8d570-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8d570-112">説明</span><span class="sxs-lookup"><span data-stu-id="8d570-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d570-113"><strong>Database File Name/データベース ファイル名</strong></span><span class="sxs-lookup"><span data-stu-id="8d570-113"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8d570-p103">新しいマスター データ ファイルの名前を指定します。このファイルの既定のパスは、Access プロジェクト ファイル (.adp) の現在の場所です。</span><span class="sxs-lookup"><span data-stu-id="8d570-p103">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d570-116"><strong>Overwrite Existing File/既存ファイルの上書き</strong></span><span class="sxs-lookup"><span data-stu-id="8d570-116"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="8d570-117">同じ名前の既存のファイルを置換するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8d570-117">Specifies whether or not to replace an existing file with the same name.</span></span> <span data-ttu-id="8d570-118">場合<strong>[はい]</strong>に設定し、ファイル名が既に存在する、ファイルは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="8d570-118">If set to <strong>Yes</strong> and the filename already exists, the file is overwritten.</span></span> <span data-ttu-id="8d570-119">場合は<strong>No</strong>に設定ファイル名が既に存在する、ファイルが上書きされないと、アクションは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8d570-119">If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails.</span></span> <span data-ttu-id="8d570-120">ファイルが既に存在しない場合、この設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="8d570-120">If the file does not already exist, this setting is ignored.</span></span> <span data-ttu-id="8d570-121">既定値は [ <strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="8d570-121">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d570-122"><strong>Disconnect All Users/全ユーザーの切断</strong></span><span class="sxs-lookup"><span data-stu-id="8d570-122"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="8d570-123">データベースからユーザーを強制的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8d570-123">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="8d570-124">場合は<strong>[はい]</strong>に設定、現在のデータベースに接続されているすべてのユーザーを切断し、データベースのコピー操作を続行できます。</span><span class="sxs-lookup"><span data-stu-id="8d570-124">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="8d570-125">場合設定<strong>なし</strong>もう 1 つまたはより多くのユーザーは、コピーのデータベース操作が失敗する、データベースに接続しています。</span><span class="sxs-lookup"><span data-stu-id="8d570-125">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="8d570-126">既定値は [ <strong>いいえ</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="8d570-126">The default is <strong>No</strong>.</span></span></p>

> [!WARNING]
> <P><span data-ttu-id="8d570-127">十分な通知を行わずにユーザーをデータベースから切断すると、データの損失を招く可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8d570-127">Disconnecting users from a database without adequate warning can lead to data loss.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8d570-128">解説</span><span class="sxs-lookup"><span data-stu-id="8d570-128">Remarks</span></span>

<span data-ttu-id="8d570-129">コピー操作は同期操作であるため、データベースのコピーが完了するまで他の操作は実行できません。</span><span class="sxs-lookup"><span data-stu-id="8d570-129">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="8d570-130">**データベースファイルのコピー**操作は、データ、データ定義、およびデータベース オブジェクトをコピーするだけでなく、既定値、テキスト制約、ルックアップ値などの拡張プロパティもコピーします。</span><span class="sxs-lookup"><span data-stu-id="8d570-130">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="8d570-131">データベースのコピー操作の要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d570-131">Requirements for copying a database:</span></span>

  - <span data-ttu-id="8d570-132">データベース ファイルをコピーする前にすべてのアプリケーションとユーザーを切断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d570-132">You must disconnect all applications and users before you copy the database file.</span></span>

  - <span data-ttu-id="8d570-133">ナビゲーション ウィンドウ以外のすべてのオブジェクトとビューを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d570-133">All objects and views except the Navigation Pane must be closed.</span></span>

  - <span data-ttu-id="8d570-134">カレント データベースはレプリケートできません。</span><span class="sxs-lookup"><span data-stu-id="8d570-134">The current database must not be replicated.</span></span>

  - <span data-ttu-id="8d570-135">サーバー データベースをコピーするには、ローカル コンピューターに Microsoft SQL Server Version 7.0 以降または SQL Server 2000 Desktop Engine が必要です。</span><span class="sxs-lookup"><span data-stu-id="8d570-135">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="8d570-136">コピー元のサーバーにある SQL Server データベースは、単一のファイル データベースであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="8d570-136">The SQL Server database on the source server must be a single file database.</span></span>

  - <span data-ttu-id="8d570-137">コピーを実行するユーザーは、コピー元とコピー先の両方の SQL Server コンピューターにおいて sysadmin ロールのメンバーである必要がありです。</span><span class="sxs-lookup"><span data-stu-id="8d570-137">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="8d570-138">モジュールの Visual Basic for Applications では、**データベースファイルのコピー**操作を実行するには、 **DoCmd**オブジェクトの**データベースファイルのコピー**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d570-138">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

