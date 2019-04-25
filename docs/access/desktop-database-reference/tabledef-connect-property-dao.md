---
title: TableDef.Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314386"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="4fb5c-102">TableDef.Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="4fb5c-102">TableDef.Connect Property (DAO)</span></span>

<span data-ttu-id="4fb5c-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fb5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fb5c-p101">リンク テーブルに関する情報を提供する値を設定します。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb5c-106">構文</span><span class="sxs-lookup"><span data-stu-id="4fb5c-106">Syntax</span></span>

<span data-ttu-id="4fb5c-107">*式* . Connect</span><span class="sxs-lookup"><span data-stu-id="4fb5c-107">expression  . Connect</span></span>

<span data-ttu-id="4fb5c-108">*式\*\*\*TableDef*\* オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-108">*expression*  A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb5c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="4fb5c-109">Remarks</span></span>

<span data-ttu-id="4fb5c-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="4fb5c-112">リンク テーブルを表す **TableDef** オブジェクトの場合、 **Connect** プロパティの設定値は、1 つまたは 2 つの部分 (データベースの種類の識別子とそのデータベースへのパス) で構成され、それぞれの末尾にセミコロンが付けられています。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="4fb5c-113">次の表に示すように、パスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="4fb5c-114">Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="4fb5c-115">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4fb5c-116">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="4fb5c-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="4fb5c-117">指定子</span><span class="sxs-lookup"><span data-stu-id="4fb5c-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="4fb5c-118">例</span><span class="sxs-lookup"><span data-stu-id="4fb5c-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-119">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="4fb5c-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-120">[database];</span><span class="sxs-lookup"><span data-stu-id="4fb5c-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="4fb5c-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="4fb5c-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-124">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="4fb5c-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-127">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="4fb5c-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-130">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="4fb5c-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-133">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="4fb5c-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-136">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="4fb5c-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-139">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="4fb5c-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="4fb5c-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="4fb5c-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="4fb5c-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-146">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="4fb5c-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="4fb5c-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="4fb5c-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="4fb5c-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-152">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="4fb5c-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="4fb5c-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="4fb5c-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="4fb5c-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="4fb5c-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-160">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="4fb5c-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-161">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="4fb5c-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="4fb5c-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-164">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="4fb5c-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-166">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="4fb5c-167">Text</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-168">Text;</span><span class="sxs-lookup"><span data-stu-id="4fb5c-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-169">drive:\path</span><span class="sxs-lookup"><span data-stu-id="4fb5c-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb5c-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="4fb5c-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-171">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="4fb5c-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-172">なし</span><span class="sxs-lookup"><span data-stu-id="4fb5c-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb5c-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="4fb5c-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-174">Exchange 4.0; MAPILEVEL=フォルダー パス; [TABLETYPE={ 0 | 1 }];[PROFILE=プロファイル;] [PWD=パスワード;] [DATABASE=データベース;]</span><span class="sxs-lookup"><span data-stu-id="4fb5c-174">Exchange 4.0; 
MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] 
[PWD=password;] 
[DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="4fb5c-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="4fb5c-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4fb5c-176">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="4fb5c-p104">Microsoft Exchange のデータの場合、必要な MAPILEVEL キーを、完全に解決されたフォルダー パス ("Mailbox - Pat SmithIAlpha/Today" など) に設定する必要があります。パスには、テーブルとして開かれるフォルダーの名前は含まれません。代わりに、そのフォルダーの名前は、**CreateTable** メソッドの引数 name として指定します。TABLETYPE キーは "0" (既定値) または "1" に設定します。"0" を設定するとフォルダーが開き、"1" に設定するとアドレス帳が開きます。PROFILE キーは、既定では現在使用中のプロファイルに設定されます。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-p104">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today"). The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method. The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book. The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="4fb5c-181">Micorosoft Access データベースのベース テーブルの場合、**Connect** プロパティ設定は長さ 0 の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="4fb5c-182">**ReturnsRecords** プロパティを設定する前に、**Connect** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-182">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="4fb5c-183">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fb5c-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>
