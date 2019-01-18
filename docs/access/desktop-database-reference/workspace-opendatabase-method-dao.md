---
title: Workspace.OpenDatabase メソッド (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ca2ccb4183a59c2b579fd4375f26aa4fd539532f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700956"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="6c50d-102">Workspace.OpenDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c50d-102">Workspace.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="6c50d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6c50d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c50d-104">**[Workspace](workspace-object-dao.md)** オブジェクト内で指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c50d-105">構文</span><span class="sxs-lookup"><span data-stu-id="6c50d-105">Syntax</span></span>

<span data-ttu-id="6c50d-106">*式*です。OpenDatabase (***名前***、***オプション***、***読み取り専用***、***接続***)</span><span class="sxs-lookup"><span data-stu-id="6c50d-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="6c50d-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6c50d-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c50d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c50d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c50d-109">名前</span><span class="sxs-lookup"><span data-stu-id="6c50d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6c50d-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="6c50d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6c50d-111">データ型</span><span class="sxs-lookup"><span data-stu-id="6c50d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6c50d-112">説明</span><span class="sxs-lookup"><span data-stu-id="6c50d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c50d-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="6c50d-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="6c50d-114">必須</span><span class="sxs-lookup"><span data-stu-id="6c50d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6c50d-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6c50d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6c50d-p101">既存の Microsoft Access データベース エンジンのデータベース ファイル名、または ODBC データ ソースのデータ ソース名 (DSN) です。この値を設定する方法の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティのトピックを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="6c50d-p101">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c50d-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="6c50d-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="6c50d-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="6c50d-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="6c50d-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6c50d-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6c50d-121">「備考」に記載されたデータベースのさまざまなオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c50d-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="6c50d-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="6c50d-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="6c50d-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="6c50d-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6c50d-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6c50d-125"><strong>True</strong> に設定すると、データベースが読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c50d-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="6c50d-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="6c50d-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="6c50d-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="6c50d-128"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6c50d-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6c50d-129">パスワードなどさまざまな接続情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="6c50d-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="6c50d-130">Return value</span></span>

<span data-ttu-id="6c50d-131">データベース</span><span class="sxs-lookup"><span data-stu-id="6c50d-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="6c50d-132">注釈</span><span class="sxs-lookup"><span data-stu-id="6c50d-132">Remarks</span></span>

<span data-ttu-id="6c50d-133">引数 options で使用できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6c50d-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c50d-134">Setting</span><span class="sxs-lookup"><span data-stu-id="6c50d-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="6c50d-135">説明</span><span class="sxs-lookup"><span data-stu-id="6c50d-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c50d-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="6c50d-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="6c50d-137">データベースを排他モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c50d-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="6c50d-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="6c50d-139">(既定値) データベースを共有モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="6c50d-140">データベースを開くと、そのデータベースは自動的に **Databases** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="6c50d-141">データベース名を使用する場合は、いくつかの考慮事項が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="6c50d-142">別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="6c50d-143">既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="6c50d-144">長さ 0 の文字列である場合 ("") とは、"ODBC;"は、*接続*ユーザーがデータベースを選択できるように登録されているすべての ODBC データ ソース名をリストするダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="6c50d-145">データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="6c50d-146">[!メモ] Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された **Database** オブジェクトを開いた方が、個々の **[TableDef](tabledef-object-dao.md)** オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="6c50d-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="6c50d-147">例</span><span class="sxs-lookup"><span data-stu-id="6c50d-147">Example</span></span>

<span data-ttu-id="6c50d-148">この例では、 **OpenDatabase** メソッドを使用して、Microsoft Access データベースと、Microsoft Access データベース エンジンに接続された 2 つの ODBC データベースを開きます。</span><span class="sxs-lookup"><span data-stu-id="6c50d-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

