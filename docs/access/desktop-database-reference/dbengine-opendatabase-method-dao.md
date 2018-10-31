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
ms.openlocfilehash: 311481a83c25df29a26610a979a67ceb38124470
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860421"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="2adf4-102">DBEngine.OpenDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="2adf4-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="2adf4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2adf4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2adf4-104">指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="2adf4-105">構文</span><span class="sxs-lookup"><span data-stu-id="2adf4-105">Syntax</span></span>

<span data-ttu-id="2adf4-106">*式*です。OpenDatabase (***名前***、***オプション***、***読み取り専用***、***接続***)</span><span class="sxs-lookup"><span data-stu-id="2adf4-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="2adf4-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2adf4-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2adf4-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2adf4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2adf4-109">名前</span><span class="sxs-lookup"><span data-stu-id="2adf4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2adf4-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="2adf4-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2adf4-111">データ型</span><span class="sxs-lookup"><span data-stu-id="2adf4-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2adf4-112">説明</span><span class="sxs-lookup"><span data-stu-id="2adf4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2adf4-113">名前</span><span class="sxs-lookup"><span data-stu-id="2adf4-113">Name</span></span></p></td>
<td><p><span data-ttu-id="2adf4-114">必須</span><span class="sxs-lookup"><span data-stu-id="2adf4-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2adf4-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="2adf4-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2adf4-p101">既存の Microsoft Access データベース ファイルの名前、または ODBC データ ソースのデータ ソース名 (DSN)。この値の設定方法の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="2adf4-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2adf4-118">選択肢</span><span class="sxs-lookup"><span data-stu-id="2adf4-118">Options</span></span></p></td>
<td><p><span data-ttu-id="2adf4-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="2adf4-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="2adf4-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="2adf4-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2adf4-121">「備考」に記載されたデータベースのさまざまなオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2adf4-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2adf4-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="2adf4-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="2adf4-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="2adf4-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="2adf4-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2adf4-125"><strong>True</strong> に設定すると、データベースが読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="2adf4-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2adf4-126">ブラウザでの</span><span class="sxs-lookup"><span data-stu-id="2adf4-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="2adf4-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="2adf4-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="2adf4-128"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="2adf4-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2adf4-129">パスワードなどさまざまな接続情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2adf4-130"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="2adf4-130"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="2adf4-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="2adf4-131">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="2adf4-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="2adf4-132">Return value</span></span>
>>>>>>> <span data-ttu-id="2adf4-133">master</span><span class="sxs-lookup"><span data-stu-id="2adf4-133">master</span></span>

<span data-ttu-id="2adf4-134">データベース</span><span class="sxs-lookup"><span data-stu-id="2adf4-134">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="2adf4-135">注釈</span><span class="sxs-lookup"><span data-stu-id="2adf4-135">Remarks</span></span>

<span data-ttu-id="2adf4-136">引数 options で使用できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2adf4-136">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2adf4-137">設定</span><span class="sxs-lookup"><span data-stu-id="2adf4-137">Setting</span></span></p></th>
<th><p><span data-ttu-id="2adf4-138">説明</span><span class="sxs-lookup"><span data-stu-id="2adf4-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2adf4-139"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="2adf4-139"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="2adf4-140">データベースを排他モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="2adf4-140">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2adf4-141"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="2adf4-141"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="2adf4-142">(既定値) データベースを共有モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="2adf4-142">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2adf4-143">データベースを開くと、そのデータベースは自動的に **Databases** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2adf4-143">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="2adf4-144">データベース名を使用する場合は、いくつかの考慮事項が適用されます。</span><span class="sxs-lookup"><span data-stu-id="2adf4-144">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="2adf4-145">別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-145">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="2adf4-146">既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-146">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="2adf4-147">長さ 0 の文字列である場合 ("") とは、"ODBC;"は、*接続*ユーザーがデータベースを選択できるように登録されているすべての ODBC データ ソース名をリストするダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2adf4-147">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="2adf4-148">データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-148">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <span data-ttu-id="2adf4-149">[!メモ] Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された **Database** オブジェクトを開いた方が、個々の [TableDef](tabledef-object-dao.md) オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="2adf4-149">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


