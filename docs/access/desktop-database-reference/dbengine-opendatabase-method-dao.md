---
title: DBEngine.OpenDatabase メソッド (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a00c61ce4cbb9cb9d6088d521f0c2bdb3cf7f573
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998076"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="32eb8-102">DBEngine.OpenDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="32eb8-102">DBEngine.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="32eb8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="32eb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32eb8-104">指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="32eb8-105">構文</span><span class="sxs-lookup"><span data-stu-id="32eb8-105">Syntax</span></span>

<span data-ttu-id="32eb8-106">*式*です。OpenDatabase (***名前***、***オプション***、***読み取り専用***、***接続***)</span><span class="sxs-lookup"><span data-stu-id="32eb8-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="32eb8-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="32eb8-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="32eb8-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32eb8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32eb8-109">名前</span><span class="sxs-lookup"><span data-stu-id="32eb8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="32eb8-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="32eb8-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="32eb8-111">データ型</span><span class="sxs-lookup"><span data-stu-id="32eb8-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="32eb8-112">説明</span><span class="sxs-lookup"><span data-stu-id="32eb8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32eb8-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="32eb8-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="32eb8-114">必須</span><span class="sxs-lookup"><span data-stu-id="32eb8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="32eb8-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="32eb8-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="32eb8-p101">既存の Microsoft Access データベース ファイルの名前、または ODBC データ ソースのデータ ソース名 (DSN)。この値の設定方法の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="32eb8-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eb8-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="32eb8-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="32eb8-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="32eb8-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eb8-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="32eb8-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="32eb8-121">「備考」に記載されたデータベースのさまざまなオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eb8-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="32eb8-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="32eb8-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="32eb8-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eb8-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="32eb8-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="32eb8-125"><strong>True</strong> に設定すると、データベースが読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="32eb8-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eb8-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="32eb8-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="32eb8-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="32eb8-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eb8-128"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="32eb8-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="32eb8-129">パスワードなどさまざまな接続情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="32eb8-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="32eb8-130">Return value</span></span>

<span data-ttu-id="32eb8-131">データベース</span><span class="sxs-lookup"><span data-stu-id="32eb8-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="32eb8-132">注釈</span><span class="sxs-lookup"><span data-stu-id="32eb8-132">Remarks</span></span>

<span data-ttu-id="32eb8-133">引数 options で使用できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="32eb8-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32eb8-134">設定</span><span class="sxs-lookup"><span data-stu-id="32eb8-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="32eb8-135">説明</span><span class="sxs-lookup"><span data-stu-id="32eb8-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32eb8-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="32eb8-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="32eb8-137">データベースを排他モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="32eb8-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eb8-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="32eb8-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="32eb8-139">(既定値) データベースを共有モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="32eb8-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32eb8-140">データベースを開くと、そのデータベースは自動的に **Databases** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="32eb8-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="32eb8-141">データベース名を使用する場合は、いくつかの考慮事項が適用されます。</span><span class="sxs-lookup"><span data-stu-id="32eb8-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="32eb8-142">別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="32eb8-143">既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="32eb8-144">長さ 0 の文字列である場合 ("") とは、"ODBC;"は、*接続*ユーザーがデータベースを選択できるように登録されているすべての ODBC データ ソース名をリストするダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32eb8-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="32eb8-145">データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="32eb8-146">[!メモ] Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された **Database** オブジェクトを開いた方が、個々の [TableDef](tabledef-object-dao.md) オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="32eb8-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


