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
ms.openlocfilehash: 322b59c6556b73186fe4034e64c75d9104d29560
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926900"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="14110-102">TableDef.Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="14110-102">TableDef.Connect property (DAO)</span></span>


<span data-ttu-id="14110-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="14110-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14110-p101">リンク テーブルに関する情報を提供する値を設定します。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="14110-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="14110-106">構文</span><span class="sxs-lookup"><span data-stu-id="14110-106">Syntax</span></span>

<span data-ttu-id="14110-107">*式*です。接続</span><span class="sxs-lookup"><span data-stu-id="14110-107">*expression* .Connect</span></span>

<span data-ttu-id="14110-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="14110-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14110-109">注釈</span><span class="sxs-lookup"><span data-stu-id="14110-109">Remarks</span></span>

<span data-ttu-id="14110-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="14110-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="14110-112">リンク テーブルを表す **TableDef** オブジェクトの場合、 **Connect** プロパティの設定値は、1 つまたは 2 つの部分 (データベースの種類の識別子とそのデータベースへのパス) で構成され、それぞれの末尾にセミコロンが付けられています。</span><span class="sxs-lookup"><span data-stu-id="14110-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="14110-p103">次の表のパスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="14110-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="14110-115">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="14110-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14110-116">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="14110-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="14110-117">識別子</span><span class="sxs-lookup"><span data-stu-id="14110-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="14110-118">例</span><span class="sxs-lookup"><span data-stu-id="14110-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14110-119">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="14110-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="14110-120">[database];</span><span class="sxs-lookup"><span data-stu-id="14110-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="14110-121"><ドライブ>:\<パス>\<ファイル名>.wk1</span><span class="sxs-lookup"><span data-stu-id="14110-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="14110-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="14110-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="14110-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="14110-124"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="14110-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="14110-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="14110-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="14110-127"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="14110-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="14110-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="14110-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="14110-130"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="14110-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="14110-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="14110-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="14110-133"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="14110-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="14110-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="14110-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="14110-136"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="14110-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="14110-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="14110-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="14110-139"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="14110-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="14110-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="14110-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="14110-142"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="14110-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="14110-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="14110-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="14110-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="14110-145"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="14110-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-146">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="14110-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="14110-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="14110-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="14110-148"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="14110-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="14110-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="14110-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="14110-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="14110-151"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="14110-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-152">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="14110-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="14110-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="14110-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="14110-154"><ドライブ>:\<パス>\<ファイル名.wk1></span><span class="sxs-lookup"><span data-stu-id="14110-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="14110-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="14110-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="14110-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="14110-157"><ドライブ>:\<パス>\<ファイル名.wk3></span><span class="sxs-lookup"><span data-stu-id="14110-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="14110-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="14110-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="14110-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="14110-160"><ドライブ>:\<パス>\<ファイル名.wk4></span><span class="sxs-lookup"><span data-stu-id="14110-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-161">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="14110-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="14110-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="14110-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="14110-163"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="14110-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-164">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="14110-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="14110-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="14110-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="14110-166"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="14110-167">Text</span></span></p></td>
<td><p><span data-ttu-id="14110-168">Text;</span><span class="sxs-lookup"><span data-stu-id="14110-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="14110-169"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="14110-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14110-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="14110-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="14110-171">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="14110-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="14110-172">なし</span><span class="sxs-lookup"><span data-stu-id="14110-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14110-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="14110-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="14110-174">Exchange 4.0 です。MAPILEVEL = folderpath です。[TABLETYPE = {0 | 1}]。[プロファイル = プロファイル][PWD = パスワード][データベース = データベース]</span><span class="sxs-lookup"><span data-stu-id="14110-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="14110-175"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="14110-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14110-176">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="14110-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="14110-177">Microsoft Exchange のデータを完全に解決済みのフォルダーのパス (たとえば、「メールボックス-Pat SmithIAlpha/今日」) に必要な MAPILEVEL キーを設定してください。</span><span class="sxs-lookup"><span data-stu-id="14110-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="14110-178">パスでは、テーブルとして表示するフォルダーの名前は含まれません**CreateTable**メソッドの引数名としてそのフォルダーの名前を指定する必要があります代わりに。</span><span class="sxs-lookup"><span data-stu-id="14110-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="14110-179">TABLETYPE キーは、フォルダー (既定値) またはアドレス帳を開くには、「1」を開く「0」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14110-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="14110-180">プロファイルにプロファイル キーの既定値が使用されています。</span><span class="sxs-lookup"><span data-stu-id="14110-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="14110-181">Micorosoft Access データベースのベース テーブルの場合、 **Connect** プロパティ設定は長さ 0 の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="14110-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="14110-182">[!メモ] <STRONG>ReturnsRecords</STRONG> プロパティを設定する前に、 <STRONG>Connect</STRONG> プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14110-182">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="14110-183">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="14110-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


