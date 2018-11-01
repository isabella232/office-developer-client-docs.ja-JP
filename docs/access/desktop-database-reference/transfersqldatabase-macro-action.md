---
title: "'TransferSQLDatabase/SQLデータベースの転送' マクロ アクション"
TOCTitle: TransferSQLDatabase Macro Action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fff0c9ac46e4a616fb5ea134e3dabc6b4e90576f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873104"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="953a4-102">"TransferSQLDatabase/SQLデータベースの転送" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="953a4-102">TransferSQLDatabase Macro Action</span></span>


<span data-ttu-id="953a4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="953a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="953a4-104">Access プロジェクトで、Microsoft SQL Server 7.0 以降のデータベースを別の SQL Server 7.0、またはそれ以降のデータベースを転送するのに**TransferSQLDatabase**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="953a4-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="953a4-105">データベースを転送することに関する詳細については、SQL Server のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="953a4-105">For more information about transferring a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <span data-ttu-id="953a4-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="953a4-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="953a4-108">設定値</span><span class="sxs-lookup"><span data-stu-id="953a4-108">Setting</span></span>

<span data-ttu-id="953a4-109">**TransferSQLDatabase**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="953a4-109">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="953a4-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="953a4-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="953a4-111">説明</span><span class="sxs-lookup"><span data-stu-id="953a4-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="953a4-112"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="953a4-112"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="953a4-113">転送先の SQL Server 7.0 以降のデータベース サーバーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="953a4-113">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953a4-114"><strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="953a4-114"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="953a4-115">転送先のサーバーに作成される新しいデータベースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="953a4-115">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="953a4-116"><strong>Use Trusted Connection/セキュリティ接続を使用する</strong></span><span class="sxs-lookup"><span data-stu-id="953a4-116"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="953a4-117">指定またはが存在しないかどうかは、SQL Server に信頼関係接続です。</span><span class="sxs-lookup"><span data-stu-id="953a4-117">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="953a4-118">場合は、信頼関係接続と<strong>ログイン名</strong>と<strong>パスワード</strong>の引数は必須ではありませんし、 <strong>[はい]</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="953a4-118">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="953a4-119"><strong>いいえ</strong>、<strong>ログイン</strong>および<strong>パスワード</strong>の引数に設定が必要な場合です。</span><span class="sxs-lookup"><span data-stu-id="953a4-119">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="953a4-120">既定値は [ <strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="953a4-120">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="953a4-121">信頼関係接続を使用すると、SQL Server のセキュリティは、ネットワークとデータベースに 1 つのログを提供する Windows オペレーティング システムのセキュリティと統合します。</span><span class="sxs-lookup"><span data-stu-id="953a4-121">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953a4-122"><strong>Login/ログイン</strong></span><span class="sxs-lookup"><span data-stu-id="953a4-122"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="953a4-123">転送先のサーバーへのログイン名を指定します。</span><span class="sxs-lookup"><span data-stu-id="953a4-123">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="953a4-124"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="953a4-124"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="953a4-125"><strong>ログイン</strong>引数のパスワード。</span><span class="sxs-lookup"><span data-stu-id="953a4-125">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="953a4-126">このパスワードは、Access プロジェクト内のテキストとして格納されますが、データベースの転送操作中に非表示。</span><span class="sxs-lookup"><span data-stu-id="953a4-126">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953a4-127"><strong>Transfer Copy Data/データ コピーの転送</strong></span><span class="sxs-lookup"><span data-stu-id="953a4-127"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="953a4-p105">データベースの転送処理にデータを含めるかどうかを指定します。[<strong>はい</strong>] に設定した場合は、すべてのテーブルのすべてのデータが、すべてのデータ構造、拡張プロパティ、およびデータベース オブジェクトと共に転送されます。[<strong>いいえ</strong>] に設定した場合は、テーブルのデータは含まれません。テーブル構造と拡張プロパティのみが、データベース ダイアグラムを除くその他すべてのデータベース オブジェクトと共に、転送先のサーバーに作成されます。既定値は [<strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="953a4-p105">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="953a4-133">解説</span><span class="sxs-lookup"><span data-stu-id="953a4-133">Remarks</span></span>

<span data-ttu-id="953a4-134">データベースの転送中は、その他の操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="953a4-134">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="953a4-135">**TransferSQLDatabase**アクションでは、既定では、コピーのデータ、データ定義、データベース オブジェクト、および既定値、テキスト制約、ルックアップ値などの拡張プロパティです。</span><span class="sxs-lookup"><span data-stu-id="953a4-135">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="953a4-136">データベースを転送するには、次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="953a4-136">There are requirements for transferring a database:</span></span>

  - <span data-ttu-id="953a4-137">操作を実行するユーザーは、転送先のサーバーにおける sysadmin ロールのメンバーであること (転送元のサーバーでは特にロールは問いません)。</span><span class="sxs-lookup"><span data-stu-id="953a4-137">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

<!-- end list -->

  - <span data-ttu-id="953a4-138">Access プロジェクトに接続されている現在の SQL サーバーと、データベースの転送先のサーバーが SQL Server Version 7.0 以降であること。</span><span class="sxs-lookup"><span data-stu-id="953a4-138">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>


> [!NOTE]
> <P><span data-ttu-id="953a4-139">[!メモ] リンク サーバーは、データベースの転送時には転送されません。</span><span class="sxs-lookup"><span data-stu-id="953a4-139">Linked servers are not transferred during a database transfer operation.</span></span></P>



<span data-ttu-id="953a4-140">**TransferSQLDatabase**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**TransferSQLDatabase**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="953a4-140">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

