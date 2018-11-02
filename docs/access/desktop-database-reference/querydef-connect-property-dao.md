---
title: QueryDef.Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1208ac064c92e2e3793e8f2e3ceb4502cbfa4d6c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922007"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="6172e-102">QueryDef.Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6172e-102">QueryDef.Connect property (DAO)</span></span>


<span data-ttu-id="6172e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6172e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6172e-p101">パススルー クエリで使用するデータベース ソースに関する情報を提供する値を設定します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6172e-p101">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6172e-106">構文</span><span class="sxs-lookup"><span data-stu-id="6172e-106">Syntax</span></span>

<span data-ttu-id="6172e-107">*式*です。接続</span><span class="sxs-lookup"><span data-stu-id="6172e-107">*expression* .Connect</span></span>

<span data-ttu-id="6172e-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6172e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6172e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="6172e-109">Remarks</span></span>

<span data-ttu-id="6172e-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="6172e-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="6172e-112">Microsoft Access データベース ファイルにリンクしているテーブルに対して SQL パススルー クエリを実行するには、まず、テーブルがリンクしているデータベースの **Connect** プロパティを、有効な ODBC 接続文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6172e-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="6172e-p103">次の表のパスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6172e-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="6172e-115">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="6172e-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6172e-116">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="6172e-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="6172e-117">識別子</span><span class="sxs-lookup"><span data-stu-id="6172e-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="6172e-118">例</span><span class="sxs-lookup"><span data-stu-id="6172e-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6172e-119">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="6172e-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="6172e-120">[database];</span><span class="sxs-lookup"><span data-stu-id="6172e-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="6172e-121"><ドライブ>:\<パス>\<ファイル名>.wk1</span><span class="sxs-lookup"><span data-stu-id="6172e-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="6172e-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="6172e-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="6172e-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="6172e-124"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="6172e-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="6172e-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="6172e-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="6172e-127"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="6172e-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="6172e-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="6172e-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="6172e-130"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="6172e-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="6172e-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="6172e-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="6172e-133"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="6172e-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="6172e-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="6172e-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="6172e-136"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="6172e-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="6172e-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="6172e-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="6172e-139"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="6172e-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="6172e-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="6172e-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="6172e-142"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="6172e-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="6172e-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="6172e-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="6172e-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="6172e-145"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="6172e-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-146">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="6172e-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="6172e-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="6172e-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="6172e-148"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="6172e-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="6172e-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="6172e-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="6172e-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="6172e-151"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="6172e-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-152">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="6172e-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="6172e-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="6172e-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="6172e-154"><ドライブ>:\<パス>\<ファイル名.wk1></span><span class="sxs-lookup"><span data-stu-id="6172e-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="6172e-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="6172e-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="6172e-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="6172e-157"><ドライブ>:\<パス>\<ファイル名.wk3></span><span class="sxs-lookup"><span data-stu-id="6172e-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="6172e-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="6172e-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="6172e-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="6172e-160"><ドライブ>:\<パス>\<ファイル名.wk4></span><span class="sxs-lookup"><span data-stu-id="6172e-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-161">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="6172e-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="6172e-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="6172e-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="6172e-163"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="6172e-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-164">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="6172e-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="6172e-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="6172e-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="6172e-166"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="6172e-167">Text</span></span></p></td>
<td><p><span data-ttu-id="6172e-168">Text;</span><span class="sxs-lookup"><span data-stu-id="6172e-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="6172e-169"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="6172e-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6172e-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="6172e-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="6172e-171">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="6172e-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="6172e-172">なし</span><span class="sxs-lookup"><span data-stu-id="6172e-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6172e-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="6172e-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="6172e-174">Exchange 4.0 です。MAPILEVEL = folderpath です。[TABLETYPE = {0 | 1}]。[プロファイル = プロファイル][PWD = パスワード][データベース = データベース]</span><span class="sxs-lookup"><span data-stu-id="6172e-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="6172e-175"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="6172e-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6172e-176">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="6172e-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="6172e-177">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6172e-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="6172e-178">Microsoft Exchange のデータを完全に解決済みのフォルダーのパス (たとえば、「メールボックス-Pat SmithIAlpha/今日」) に必要な MAPILEVEL キーを設定してください。</span><span class="sxs-lookup"><span data-stu-id="6172e-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="6172e-179">パスでは、テーブルとして表示するフォルダーの名前は含まれません**CreateTable**メソッドの引数名としてそのフォルダーの名前を指定する必要があります代わりに。</span><span class="sxs-lookup"><span data-stu-id="6172e-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="6172e-180">TABLETYPE キーは、フォルダー (既定値) またはアドレス帳を開くには、「1」を開く「0」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6172e-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="6172e-181">プロファイルにプロファイル キーの既定値が使用されています。</span><span class="sxs-lookup"><span data-stu-id="6172e-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="6172e-182">Microsoft Access ワークスペースの **QueryDef** オブジェクトの場合、 **Connect** プロパティを ReturnsRecords プロパティと共に使用すると、ODBC SQL パススルー クエリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6172e-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="6172e-183">"ODBC;"では、接続文字列のされていませんし、文字列の残りの部分には、リモート データにアクセスするために使用する ODBC ドライバーに固有の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6172e-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="6172e-184">詳細については、それぞれのドライバーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6172e-184">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="6172e-185">先に <STRONG>Connect</STRONG> プロパティを設定してから、 <STRONG>ReturnsRecords</STRONG> プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6172e-185">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="6172e-186">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6172e-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


