---
title: DBEngine.OpenConnection メソッド (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704603"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="ab68c-102">DBEngine.OpenConnection メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ab68c-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="ab68c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ab68c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="ab68c-104">構文</span><span class="sxs-lookup"><span data-stu-id="ab68c-104">Syntax</span></span>

<span data-ttu-id="ab68c-105">*式*です。されます (***名前***、***オプション***、***読み取り専用***、***接続***)</span><span class="sxs-lookup"><span data-stu-id="ab68c-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="ab68c-106">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ab68c-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab68c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab68c-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab68c-108">名前</span><span class="sxs-lookup"><span data-stu-id="ab68c-108">Name</span></span></p></th>
<th><p><span data-ttu-id="ab68c-109">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="ab68c-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ab68c-110">データ型</span><span class="sxs-lookup"><span data-stu-id="ab68c-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="ab68c-111">説明</span><span class="sxs-lookup"><span data-stu-id="ab68c-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab68c-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ab68c-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ab68c-113">必須</span><span class="sxs-lookup"><span data-stu-id="ab68c-113">Required</span></span></p></td>
<td><p><span data-ttu-id="ab68c-114"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-p101">文字列式を指定します。「解説」の説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p101">A string expression. See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab68c-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="ab68c-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="ab68c-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="ab68c-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab68c-119"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-p102">「解説」に記載されている接続のさまざまなオプションを設定します。ODBC ドライバー マネージャーは、この値に基づき、データ ソース名 (DSN)、ユーザー名、パスワードなどの接続情報の指定をユーザーに求めます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab68c-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="ab68c-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="ab68c-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="ab68c-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab68c-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-125"><strong>True</strong> に設定すると、接続が読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab68c-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="ab68c-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="ab68c-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="ab68c-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab68c-128"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-129">ODBC 接続文字列です。</span><span class="sxs-lookup"><span data-stu-id="ab68c-129">An ODBC connection string.</span></span> <span data-ttu-id="ab68c-130">この文字列の固有の要素および構文については、 <strong><a href="connection-connect-property-dao.md">Connect</a></strong> プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab68c-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="ab68c-131">先頭に追加された&quot;ODBC;&quot;が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab68c-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ab68c-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="ab68c-132">Return value</span></span>

<span data-ttu-id="ab68c-133">Connection</span><span class="sxs-lookup"><span data-stu-id="ab68c-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="ab68c-134">注釈</span><span class="sxs-lookup"><span data-stu-id="ab68c-134">Remarks</span></span>

<span data-ttu-id="ab68c-p104">**OpenConnection** メソッドは、ODBCDirect ワークスペースから ODBC データ ソースへの接続を確立するために使用します。 **OpenConnection** メソッドは、 **OpenDatabase** と似ていますが、同じではありません。主な違いは、 **OpenConnection** が ODBCDirect ワークスペースでしか使用できないことです。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="ab68c-138">登録済みの ODBC データ ソース名 (DSN) を指定すると、接続の引数で、引数 name は任意の有効な文字列を使用でき、**接続**オブジェクトの**Name**プロパティも提供されます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="ab68c-139">接続の引数には、有効な DSN が含まれていない場合、名前は、 **Name**プロパティもありますが、有効な ODBC DSN を参照しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ab68c-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="ab68c-140">場合名前し、接続のどちらも、有効な DSN が含まれている ODBC ドライバ ・ マネージャーは、ユーザーに必要な接続情報を要求する (オプションの引数) を使用して設定できます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="ab68c-141">この場合、ユーザーが指定した DSN が **Name** プロパティの値となります。</span><span class="sxs-lookup"><span data-stu-id="ab68c-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="ab68c-p106">引数 options では、接続を確立するための情報の入力をユーザーに求めるかどうか、どのような場合にユーザー入力を求めるか、接続を非同期で開くかどうかを指定します。次のいずれかの定数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p106">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously. You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab68c-144">定数</span><span class="sxs-lookup"><span data-stu-id="ab68c-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="ab68c-145">説明</span><span class="sxs-lookup"><span data-stu-id="ab68c-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab68c-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-p107">ODBC ドライバー マネージャーは、<em>name</em> および <em>connect</em> に指定された接続文字列を使用します。情報が不足していると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p107">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>. If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab68c-149"><strong>そのまま使用</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-p108">ODBC ドライバー マネージャーは、<em>dhname</em> または <em>connect</em> で指定された関連情報を示す [<strong>接続する ODBC データ ソース</strong>] ダイアログ ボックスを開きます。接続文字列は、ユーザーがダイアログ ボックスで選択した DSN を使用して作成されますが、ユーザーが DSN を指定しなかった場合は、既定の DSN が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab68c-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-p109">既定値です。引数 <em>connect</em> で接続の確立に必要な情報がすべて指定されている場合、ODBC ドライバー マネージャーは <em>connect</em> で指定されている文字列を使用します。指定されていない情報がある場合は、<strong>dbDriverPrompt</strong> を指定したときと同じ動作を行います。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab68c-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-157">このオプションを指定した場合の動作は <strong>dbDriverComplete</strong> の場合と似ていますが、接続を確立するために不足している情報についてのみユーザー入力を求める点が異なります。</span><span class="sxs-lookup"><span data-stu-id="ab68c-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab68c-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="ab68c-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="ab68c-159">メソッドを非同期で実行します。</span><span class="sxs-lookup"><span data-stu-id="ab68c-159">Execute the method asynchronously.</span></span> <span data-ttu-id="ab68c-160">この定数は、他の<em>オプション</em>の定数のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab68c-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab68c-p111">**OpenConnection** は、接続に関する情報を含む **Connection** オブジェクトを返します。 **Connection** オブジェクトは **[Database](database-object-dao.md)** オブジェクトに似ています。主な違いは、 **Database** オブジェクトは通常データベースを表すものの、Microsoft Access ワークスペースから ODBC データ ソースへの接続を表すためにも使用できることです。</span><span class="sxs-lookup"><span data-stu-id="ab68c-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

