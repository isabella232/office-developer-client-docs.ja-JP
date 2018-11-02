---
title: Database.Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a6af1ee460cc06d37fe031fe5488badd8b56ad6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925759"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="58659-102">Database.Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="58659-102">Database.Connect property (DAO)</span></span>


<span data-ttu-id="58659-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="58659-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="58659-p101">開いているデータベースのソースに関する情報を提供する値を設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="58659-p101">Sets or returns a value that provides information about the source an open database. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="58659-106">構文</span><span class="sxs-lookup"><span data-stu-id="58659-106">Syntax</span></span>

<span data-ttu-id="58659-107">*式*です。接続</span><span class="sxs-lookup"><span data-stu-id="58659-107">*expression* .Connect</span></span>

<span data-ttu-id="58659-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="58659-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="58659-109">注釈</span><span class="sxs-lookup"><span data-stu-id="58659-109">Remarks</span></span>

<span data-ttu-id="58659-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="58659-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="58659-112">Microsoft Access データベース ファイルにリンクしているテーブルに対して SQL パススルー クエリを実行するには、まず、テーブルがリンクしているデータベースの **Connect** プロパティを、有効な ODBC 接続文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58659-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="58659-p103">次の表のパスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="58659-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="58659-115">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="58659-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58659-116">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="58659-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="58659-117">識別子</span><span class="sxs-lookup"><span data-stu-id="58659-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="58659-118">例</span><span class="sxs-lookup"><span data-stu-id="58659-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58659-119">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="58659-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="58659-120">[database];</span><span class="sxs-lookup"><span data-stu-id="58659-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="58659-121"><ドライブ>:\<パス>\<ファイル名>.wk1</span><span class="sxs-lookup"><span data-stu-id="58659-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="58659-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="58659-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="58659-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="58659-124"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="58659-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="58659-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="58659-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="58659-127"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="58659-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="58659-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="58659-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="58659-130"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="58659-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="58659-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="58659-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="58659-133"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="58659-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="58659-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="58659-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="58659-136"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="58659-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="58659-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="58659-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="58659-139"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="58659-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="58659-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="58659-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="58659-142"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="58659-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="58659-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="58659-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="58659-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="58659-145"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="58659-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-146">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="58659-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="58659-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="58659-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="58659-148"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="58659-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="58659-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="58659-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="58659-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="58659-151"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="58659-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-152">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="58659-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="58659-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="58659-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="58659-154"><ドライブ>:\<パス>\<ファイル名.wk1></span><span class="sxs-lookup"><span data-stu-id="58659-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="58659-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="58659-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="58659-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="58659-157"><ドライブ>:\<パス>\<ファイル名.wk3></span><span class="sxs-lookup"><span data-stu-id="58659-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="58659-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="58659-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="58659-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="58659-160"><ドライブ>:\<パス>\<ファイル名.wk4></span><span class="sxs-lookup"><span data-stu-id="58659-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-161">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="58659-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="58659-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="58659-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="58659-163"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="58659-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-164">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="58659-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="58659-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="58659-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="58659-166"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="58659-167">Text</span></span></p></td>
<td><p><span data-ttu-id="58659-168">Text;</span><span class="sxs-lookup"><span data-stu-id="58659-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="58659-169"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="58659-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58659-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="58659-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="58659-171">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="58659-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="58659-172">なし</span><span class="sxs-lookup"><span data-stu-id="58659-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58659-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="58659-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="58659-174">Exchange 4.0 です。MAPILEVEL = folderpath です。[TABLETYPE = {0 | 1}]。[プロファイル = プロファイル][PWD = パスワード][データベース = データベース]</span><span class="sxs-lookup"><span data-stu-id="58659-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="58659-175"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="58659-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58659-176">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="58659-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="58659-177">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="58659-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="58659-178">Microsoft Exchange のデータを完全に解決済みのフォルダーのパス (たとえば、「メールボックス-Pat SmithIAlpha/今日」) に必要な MAPILEVEL キーを設定してください。</span><span class="sxs-lookup"><span data-stu-id="58659-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="58659-179">パスでは、テーブルとして表示するフォルダーの名前は含まれません**CreateTable**メソッドの引数名としてそのフォルダーの名前を指定する必要があります代わりに。</span><span class="sxs-lookup"><span data-stu-id="58659-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="58659-180">TABLETYPE キーは、フォルダー (既定値) またはアドレス帳を開くには、「1」を開く「0」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58659-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="58659-181">プロファイルにプロファイル キーの既定値が使用されています。</span><span class="sxs-lookup"><span data-stu-id="58659-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="58659-p105">**Database** オブジェクトの **Connect** プロパティを設定するには、 **OpenDatabase** メソッドに引数 source を指定します。設定を確認すると、データベースの種類、ユーザー ID、パスワード、または ODBC データ ソースを確かめることができます。</span><span class="sxs-lookup"><span data-stu-id="58659-p105">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method. You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="58659-184">先に **Connect** プロパティを設定してから、 **ReturnsRecords** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58659-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="58659-185">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="58659-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


