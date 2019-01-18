---
title: TransferSQLDatabase マクロ アクション
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711491"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="ae6f8-102">TransferSQLDatabase マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ae6f8-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="ae6f8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae6f8-104">Access プロジェクトで、Microsoft SQL Server 7.0 以降のデータベースを別の SQL Server 7.0、またはそれ以降のデータベースを転送するのに**TransferSQLDatabase**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="ae6f8-105">データベースを転送することに関する詳細については、SQL Server のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="ae6f8-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="ae6f8-107">設定値</span><span class="sxs-lookup"><span data-stu-id="ae6f8-107">Setting</span></span>

<span data-ttu-id="ae6f8-108">**TransferSQLDatabase**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae6f8-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="ae6f8-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ae6f8-110">説明</span><span class="sxs-lookup"><span data-stu-id="ae6f8-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae6f8-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ae6f8-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ae6f8-112">転送先の SQL Server 7.0 以降のデータベース サーバーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6f8-113"><strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="ae6f8-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="ae6f8-114">転送先のサーバーに作成される新しいデータベースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6f8-115"><strong>Use Trusted Connection/セキュリティ接続を使用する</strong></span><span class="sxs-lookup"><span data-stu-id="ae6f8-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="ae6f8-116">指定またはが存在しないかどうかは、SQL Server に信頼関係接続です。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="ae6f8-117">場合は、信頼関係接続と<strong>ログイン名</strong>と<strong>パスワード</strong>の引数は必須ではありませんし、 <strong>[はい]</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="ae6f8-118"><strong>いいえ</strong>、<strong>ログイン</strong>および<strong>パスワード</strong>の引数に設定が必要な場合です。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="ae6f8-119">既定値は [ <strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="ae6f8-120">信頼関係接続を使用すると、SQL Server のセキュリティは、ネットワークとデータベースに 1 つのログを提供する Windows オペレーティング システムのセキュリティと統合します。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6f8-121"><strong>Login/ログイン</strong></span><span class="sxs-lookup"><span data-stu-id="ae6f8-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="ae6f8-122">転送先のサーバーへのログイン名を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6f8-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="ae6f8-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="ae6f8-124"><strong>ログイン</strong>引数のパスワード。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-124">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="ae6f8-125">このパスワードは、Access プロジェクト内のテキストとして格納されますが、データベースの転送操作中に非表示。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-125">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6f8-126"><strong>Transfer Copy Data/データ コピーの転送</strong></span><span class="sxs-lookup"><span data-stu-id="ae6f8-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="ae6f8-p104">データベースの転送処理にデータを含めるかどうかを指定します。[<strong>はい</strong>] に設定した場合は、すべてのテーブルのすべてのデータが、すべてのデータ構造、拡張プロパティ、およびデータベース オブジェクトと共に転送されます。[<strong>いいえ</strong>] に設定した場合は、テーブルのデータは含まれません。テーブル構造と拡張プロパティのみが、データベース ダイアグラムを除くその他すべてのデータベース オブジェクトと共に、転送先のサーバーに作成されます。既定値は [<strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-p104">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ae6f8-132">解説</span><span class="sxs-lookup"><span data-stu-id="ae6f8-132">Remarks</span></span>

<span data-ttu-id="ae6f8-133">データベースの転送中は、その他の操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="ae6f8-134">**TransferSQLDatabase**アクションでは、既定では、コピーのデータ、データ定義、データベース オブジェクト、および既定値、テキスト制約、ルックアップ値などの拡張プロパティです。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="ae6f8-135">データベースを転送するには、次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="ae6f8-136">操作を実行するユーザーは、転送先のサーバーにおける sysadmin ロールのメンバーであること (転送元のサーバーでは特にロールは問いません)。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="ae6f8-137">Access プロジェクトに接続されている現在の SQL サーバーと、データベースの転送先のサーバーが SQL Server Version 7.0 以降であること。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ae6f8-138">[!メモ] リンク サーバーは、データベースの転送時には転送されません。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="ae6f8-139">**TransferSQLDatabase**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**TransferSQLDatabase**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae6f8-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

