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
ms.openlocfilehash: 54078705c67e892b80a08ce2bd31db191c7fc70c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606159"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="6dd54-102">DBEngine.OpenDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="6dd54-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="6dd54-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dd54-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6dd54-104">指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd54-105">構文</span><span class="sxs-lookup"><span data-stu-id="6dd54-105">Syntax</span></span>

<span data-ttu-id="6dd54-106">*式*です。OpenDatabase (***名前***、***オプション***、***読み取り専用***、***接続***)</span><span class="sxs-lookup"><span data-stu-id="6dd54-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="6dd54-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6dd54-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="6dd54-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6dd54-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6dd54-109">名前</span><span class="sxs-lookup"><span data-stu-id="6dd54-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6dd54-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="6dd54-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6dd54-111">データ型</span><span class="sxs-lookup"><span data-stu-id="6dd54-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="6dd54-112">説明</span><span class="sxs-lookup"><span data-stu-id="6dd54-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dd54-113">名前</span><span class="sxs-lookup"><span data-stu-id="6dd54-113">Name</span></span></p></td>
<td><p><span data-ttu-id="6dd54-114">必須</span><span class="sxs-lookup"><span data-stu-id="6dd54-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6dd54-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6dd54-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd54-p101">既存の Microsoft Access データベース ファイルの名前、または ODBC データ ソースのデータ ソース名 (DSN)。この値の設定方法の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="6dd54-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd54-118">選択肢</span><span class="sxs-lookup"><span data-stu-id="6dd54-118">Options</span></span></p></td>
<td><p><span data-ttu-id="6dd54-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="6dd54-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="6dd54-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6dd54-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd54-121">「備考」に記載されたデータベースのさまざまなオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dd54-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6dd54-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6dd54-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="6dd54-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="6dd54-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6dd54-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd54-125"><strong>True</strong> に設定すると、データベースが読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="6dd54-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd54-126">ブラウザでの</span><span class="sxs-lookup"><span data-stu-id="6dd54-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="6dd54-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="6dd54-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="6dd54-128"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6dd54-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd54-129">パスワードなどさまざまな接続情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dd54-130"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="6dd54-130"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="6dd54-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="6dd54-131">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="6dd54-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="6dd54-132">Return value</span></span>
>>>>>>> <span data-ttu-id="6dd54-133">master</span><span class="sxs-lookup"><span data-stu-id="6dd54-133">master</span></span>

<span data-ttu-id="6dd54-134">データベース</span><span class="sxs-lookup"><span data-stu-id="6dd54-134">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="6dd54-135">注釈</span><span class="sxs-lookup"><span data-stu-id="6dd54-135">Remarks</span></span>

<span data-ttu-id="6dd54-136">引数 options で使用できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6dd54-136">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6dd54-137">設定</span><span class="sxs-lookup"><span data-stu-id="6dd54-137">Setting</span></span></p></th>
<th><p><span data-ttu-id="6dd54-138">説明</span><span class="sxs-lookup"><span data-stu-id="6dd54-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dd54-139"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="6dd54-139"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd54-140">データベースを排他モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="6dd54-140">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd54-141"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="6dd54-141"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd54-142">(既定値) データベースを共有モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="6dd54-142">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dd54-143">データベースを開くと、そのデータベースは自動的に **Databases** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="6dd54-143">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="6dd54-144">データベース名を使用する場合は、いくつかの考慮事項が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6dd54-144">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="6dd54-145">別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-145">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="6dd54-146">既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-146">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="6dd54-147">長さ 0 の文字列である場合 ("") とは、"ODBC;"は、*接続*ユーザーがデータベースを選択できるように登録されているすべての ODBC データ ソース名をリストするダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6dd54-147">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="6dd54-148">データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-148">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6dd54-149">[!メモ] Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された <STRONG>Database</STRONG> オブジェクトを開いた方が、個々の <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="6dd54-149">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a <STRONG>Database</STRONG> object connected to the ODBC data source, rather than by linking individual <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> objects to specific tables in the ODBC data source.</span></span></P>


