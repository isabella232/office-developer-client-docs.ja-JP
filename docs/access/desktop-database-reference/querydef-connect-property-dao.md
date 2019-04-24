---
title: Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301086"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="783fa-102">Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="783fa-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="783fa-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="783fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="783fa-104">パススルークエリで使用されるデータベースのソースについての情報を提供する値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="783fa-104">Sets or returns a value that provides information about the source of database used in a pass-through query.</span></span> <span data-ttu-id="783fa-105">値の取得のみ可能な文字列型 (**String**) の値です。</span><span class="sxs-lookup"><span data-stu-id="783fa-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="783fa-106">構文</span><span class="sxs-lookup"><span data-stu-id="783fa-106">Syntax</span></span>

<span data-ttu-id="783fa-107">*式*。結び付ける</span><span class="sxs-lookup"><span data-stu-id="783fa-107">*expression* .Connect</span></span>

<span data-ttu-id="783fa-108">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="783fa-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="783fa-109">注釈</span><span class="sxs-lookup"><span data-stu-id="783fa-109">Remarks</span></span>

<span data-ttu-id="783fa-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="783fa-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="783fa-112">Microsoft Access データベース ファイルにリンクしているテーブルに対して SQL パススルー クエリを実行するには、まず、テーブルがリンクしているデータベースの **Connect** プロパティを、有効な ODBC 接続文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="783fa-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="783fa-113">次の表に示すように、パスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="783fa-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="783fa-114">Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="783fa-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="783fa-115">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="783fa-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="783fa-116">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="783fa-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="783fa-117">識別子</span><span class="sxs-lookup"><span data-stu-id="783fa-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="783fa-118">例</span><span class="sxs-lookup"><span data-stu-id="783fa-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="783fa-119">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="783fa-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="783fa-120">[database];</span><span class="sxs-lookup"><span data-stu-id="783fa-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="783fa-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="783fa-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="783fa-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="783fa-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="783fa-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="783fa-124">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="783fa-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="783fa-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="783fa-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="783fa-127">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="783fa-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="783fa-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="783fa-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="783fa-130">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="783fa-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="783fa-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="783fa-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="783fa-133">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="783fa-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="783fa-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="783fa-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="783fa-136">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="783fa-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="783fa-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="783fa-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="783fa-139">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="783fa-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="783fa-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="783fa-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="783fa-142">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="783fa-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="783fa-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="783fa-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="783fa-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="783fa-145">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="783fa-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-146">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="783fa-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="783fa-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="783fa-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="783fa-148">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="783fa-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="783fa-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="783fa-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="783fa-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="783fa-151">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="783fa-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-152">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="783fa-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="783fa-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="783fa-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="783fa-154">ドライブ: \ path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="783fa-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="783fa-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="783fa-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="783fa-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="783fa-157">ドライブ: \ path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="783fa-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="783fa-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="783fa-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="783fa-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="783fa-160">ドライブ: \ path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="783fa-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-161">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="783fa-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="783fa-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="783fa-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="783fa-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="783fa-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-164">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="783fa-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="783fa-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="783fa-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="783fa-166">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="783fa-167">Text</span></span></p></td>
<td><p><span data-ttu-id="783fa-168">Text;</span><span class="sxs-lookup"><span data-stu-id="783fa-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="783fa-169">drive:\path</span><span class="sxs-lookup"><span data-stu-id="783fa-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783fa-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="783fa-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="783fa-171">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="783fa-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="783fa-172">なし</span><span class="sxs-lookup"><span data-stu-id="783fa-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783fa-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="783fa-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="783fa-174">Exchange 4.0MAPILEVEL = folderpath、[TABLETYPE = {0 | 1}];[profile = profile;][PWD = password;][database = database;]</span><span class="sxs-lookup"><span data-stu-id="783fa-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="783fa-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="783fa-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="783fa-176">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="783fa-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="783fa-177">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="783fa-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="783fa-p104">Microsoft Exchange のデータの場合、必要な MAPILEVEL キーを、完全に解決されたフォルダー パス ("Mailbox - Pat SmithIAlpha/Today" など) に設定する必要があります。パスには、テーブルとして開かれるフォルダーの名前は含まれません。代わりに、そのフォルダーの名前は、**CreateTable** メソッドの引数 name として指定します。TABLETYPE キーは "0" (既定値) または "1" に設定します。"0" を設定するとフォルダーが開き、"1" に設定するとアドレス帳が開きます。PROFILE キーは、既定では現在使用中のプロファイルに設定されます。</span><span class="sxs-lookup"><span data-stu-id="783fa-p104">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today"). The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method. The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book. The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="783fa-182">Microsoft Access ワークスペースの **QueryDef** オブジェクトの場合、 **Connect** プロパティを ReturnsRecords プロパティと共に使用すると、ODBC SQL パススルー クエリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="783fa-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="783fa-183">接続文字列の databasetype は "ODBC;" で、文字列の残りの部分には、リモート データへのアクセスに使用される ODBC ドライバーに固有の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="783fa-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="783fa-184">詳細については、ODBC ドライバーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="783fa-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="783fa-185">先に **Connect** プロパティを設定してから、 **ReturnsRecords** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="783fa-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="783fa-186">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="783fa-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


