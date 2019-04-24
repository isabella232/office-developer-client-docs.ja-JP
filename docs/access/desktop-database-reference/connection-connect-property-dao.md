---
title: Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295927"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="1a870-102">Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a870-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="1a870-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a870-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a870-p101">開いている接続のソースに関する情報を提供する値を設定または取得します。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a870-p101">Sets or returns a value that provides information about the source of an open connection. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a870-106">構文</span><span class="sxs-lookup"><span data-stu-id="1a870-106">Syntax</span></span>

<span data-ttu-id="1a870-107">*式*。結び付ける</span><span class="sxs-lookup"><span data-stu-id="1a870-107">*expression* .Connect</span></span>

<span data-ttu-id="1a870-108">\*式\***Connection**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a870-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a870-109">注釈</span><span class="sxs-lookup"><span data-stu-id="1a870-109">Remarks</span></span>

<span data-ttu-id="1a870-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="1a870-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="1a870-112">Microsoft Access データベース ファイルにリンクしているテーブルに対して SQL パススルー クエリを実行するには、まず、テーブルがリンクしているデータベースの **Connect** プロパティを、有効な ODBC 接続文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a870-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="1a870-113">リンク テーブルを表す **TableDef** オブジェクトの場合、 **Connect** プロパティの設定値は、1 つまたは 2 つの部分 (データベースの種類の識別子とそのデータベースへのパス) で構成され、それぞれの末尾にセミコロンが付けられています。</span><span class="sxs-lookup"><span data-stu-id="1a870-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="1a870-114">次の表に示すように、パスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a870-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="1a870-115">Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a870-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="1a870-116">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="1a870-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a870-117">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="1a870-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="1a870-118">識別子</span><span class="sxs-lookup"><span data-stu-id="1a870-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="1a870-119">例</span><span class="sxs-lookup"><span data-stu-id="1a870-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a870-120">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="1a870-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="1a870-121">[database];</span><span class="sxs-lookup"><span data-stu-id="1a870-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="1a870-122">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="1a870-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="1a870-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="1a870-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="1a870-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="1a870-125">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="1a870-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="1a870-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="1a870-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="1a870-128">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="1a870-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="1a870-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="1a870-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="1a870-131">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="1a870-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="1a870-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="1a870-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="1a870-134">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="1a870-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="1a870-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="1a870-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="1a870-137">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="1a870-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="1a870-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="1a870-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="1a870-140">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="1a870-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="1a870-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="1a870-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="1a870-143">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="1a870-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="1a870-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="1a870-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="1a870-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="1a870-146">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="1a870-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-147">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="1a870-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="1a870-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="1a870-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="1a870-149">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="1a870-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="1a870-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="1a870-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="1a870-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="1a870-152">ドライブ: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="1a870-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-153">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="1a870-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="1a870-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="1a870-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="1a870-155">ドライブ: \ path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="1a870-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="1a870-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="1a870-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="1a870-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="1a870-158">ドライブ: \ path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="1a870-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="1a870-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="1a870-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="1a870-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="1a870-161">ドライブ: \ path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="1a870-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-162">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="1a870-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="1a870-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="1a870-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="1a870-164">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="1a870-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-165">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="1a870-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="1a870-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="1a870-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="1a870-167">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-168">テキスト</span><span class="sxs-lookup"><span data-stu-id="1a870-168">Text</span></span></p></td>
<td><p><span data-ttu-id="1a870-169">Text;</span><span class="sxs-lookup"><span data-stu-id="1a870-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="1a870-170">drive:\path</span><span class="sxs-lookup"><span data-stu-id="1a870-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a870-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="1a870-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="1a870-172">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="1a870-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="1a870-173">なし</span><span class="sxs-lookup"><span data-stu-id="1a870-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a870-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="1a870-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="1a870-175">Exchange 4.0MAPILEVEL = folderpath、[TABLETYPE = {0 | 1}];[profile = profile;][PWD = password;][database = database;]</span><span class="sxs-lookup"><span data-stu-id="1a870-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="1a870-176">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="1a870-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a870-177">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="1a870-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="1a870-178">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1a870-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="1a870-p104">Microsoft Exchange のデータの場合、必要な MAPILEVEL キーを、完全に解決されたフォルダー パス ("Mailbox - Pat SmithIAlpha/Today" など) に設定する必要があります。パスには、テーブルとして開かれるフォルダーの名前は含まれません。代わりに、そのフォルダーの名前は、**CreateTable** メソッドの引数 name として指定します。TABLETYPE キーは "0" (既定値) または "1" に設定します。"0" を設定するとフォルダーが開き、"1" に設定するとアドレス帳が開きます。PROFILE キーは、既定では現在使用中のプロファイルに設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a870-p104">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today"). The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method. The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book. The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="1a870-183">Micorosoft Access データベースのベース テーブルの場合、**Connect** プロパティ設定は長さ 0 の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="1a870-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="1a870-p105">**Database** オブジェクトの **Connect** プロパティを設定するには、 **OpenDatabase** メソッドに引数 source を指定します。設定を確認すると、データベースの種類、ユーザー ID、パスワード、または ODBC データ ソースを確かめることができます。</span><span class="sxs-lookup"><span data-stu-id="1a870-p105">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method. You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="1a870-186">Microsoft Access ワークスペースの **QueryDef** オブジェクトの場合、 **Connect** プロパティを ReturnsRecords プロパティと共に使用すると、ODBC SQL パススルー クエリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1a870-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="1a870-187">接続文字列の databasetype は "ODBC;" で、文字列の残りの部分には、リモート データへのアクセスに使用される ODBC ドライバーに固有の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a870-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="1a870-188">詳細については、ODBC ドライバーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a870-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="1a870-189">先に **Connect** プロパティを設定してから、 **ReturnsRecords** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a870-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="1a870-190">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a870-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


