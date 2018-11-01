---
title: Microsoft OLE DB Provider for Microsoft Active Directory Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1555883ef8305225d6ddd1969d98de082288a6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887538"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="e5df3-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span><span class="sxs-lookup"><span data-stu-id="e5df3-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="e5df3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e5df3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5df3-p101">Microsoft Active Directory Service Interfaces (ADSI) プロバイダーを使用すると、ADO から ADSI をとおして異種ディレクトリ サービスに接続できます。これによって、ADO アプリケーションでは、Microsoft Windows NT 4.0 および Microsoft Windows 2000 のディレクトリ サービス、LDAP 準拠のディレクトリ サービス、および Novell Directory Services に対する読み取り専用アクセスが可能になります。ADSI 自体がプロバイダー モデルに基づいているので、新しいプロバイダーで別のディレクトリへのアクセスを提供する場合でも、ADO アプリケーションはシームレスにアクセスできます。ADSI プロバイダーはフリースレッドであり、Unicode に対応しています。</span><span class="sxs-lookup"><span data-stu-id="e5df3-p101">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI. This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services. ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly. The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="e5df3-108">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="e5df3-108">Connection String Parameters</span></span>

<span data-ttu-id="e5df3-109">このプロバイダーに接続するには、**ConnectionString** プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="e5df3-110">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="e5df3-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="e5df3-111">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="e5df3-111">Typical Connection String</span></span>

<span data-ttu-id="e5df3-112">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="e5df3-113">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="e5df3-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5df3-114">キーワード</span><span class="sxs-lookup"><span data-stu-id="e5df3-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="e5df3-115">説明</span><span class="sxs-lookup"><span data-stu-id="e5df3-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-116"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="e5df3-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="e5df3-117">OLE DB Provider for Microsoft Active Directory Service を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-118"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="e5df3-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e5df3-p102">ユーザー名を指定します。このキーワードを省略すると、現在のログオンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5df3-p102">Specifies the user name. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="e5df3-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="e5df3-p103">ユーザー パスワードを指定します。このキーワードを省略すると、現在のログオンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5df3-p103">Specifies the user password. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e5df3-124">**コマンド テキスト**</span><span class="sxs-lookup"><span data-stu-id="e5df3-124">**Command Text**</span></span>

<span data-ttu-id="e5df3-125">このプロバイダーで認識されるコマンド テキストの文字列は 4 つの値で構成され、その構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5df3-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5df3-126">値</span><span class="sxs-lookup"><span data-stu-id="e5df3-126">Value</span></span></p></th>
<th><p><span data-ttu-id="e5df3-127">説明</span><span class="sxs-lookup"><span data-stu-id="e5df3-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="e5df3-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="e5df3-129">検索を開始する <strong>ADsPath</strong> オブジェクト (つまり、検索のルート) を示します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="e5df3-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="e5df3-131">RFC 1960 形式の検索フィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-132"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="e5df3-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="e5df3-133">返される属性をコンマ区切りの一覧で示します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-134"><em>スコープ</em></span><span class="sxs-lookup"><span data-stu-id="e5df3-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="e5df3-135">省略可能。</span><span class="sxs-lookup"><span data-stu-id="e5df3-135">Optional.</span></span> <span data-ttu-id="e5df3-136">検索のスコープを指定する<strong>文字列</strong>です。</span><span class="sxs-lookup"><span data-stu-id="e5df3-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="e5df3-137">次のいずれか: 基本: ベース オブジェクト (検索のルート) のみを検索します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="e5df3-138">1 レベル-は、1 レベルのみを検索します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="e5df3-139">サブツリー-は、サブツリー全体を検索します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e5df3-140">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="e5df3-p105">このプロバイダーは、コマンド テキストとして SQL SELECT もサポートしています。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e5df3-p105">The provider also supports SQL SELECT for command text. For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="e5df3-p106">このプロバイダーはストアド プロシージャの呼び出しや単純なテーブル名 (たとえば、[CommandType](commandtype-property-ado.md) が常に **adCmdText** である場合など) を受け付けません。コマンド テキストの要素の詳細については、Active Directory Service Interfaces のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5df3-p106">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**). See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="e5df3-145">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="e5df3-145">Recordset Behavior</span></span>

<span data-ttu-id="e5df3-146">次の表は、このプロバイダーで開かれた [Recordset](recordset-object-ado.md) オブジェクトで利用可能な機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="e5df3-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="e5df3-147">静的カーソルの種類 (**adOpenStatic**) のみがあります。</span><span class="sxs-lookup"><span data-stu-id="e5df3-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="e5df3-148">プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 [Recordset](properties-collection-ado.md) の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e5df3-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="e5df3-149">標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5df3-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5df3-150">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5df3-150">Property</span></span></p></th>
<th><p><span data-ttu-id="e5df3-151">利用可能性</span><span class="sxs-lookup"><span data-stu-id="e5df3-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-153">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-155">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-157">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-159">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-161">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-163">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-165">常に <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="e5df3-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-166"><a href="cursortype-property-ado.md">カーソル。</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-167">常に <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="e5df3-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-169">常に <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="e5df3-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-171">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-173">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-174"><a href="locktype-property-ado.md">ロック。</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-175">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-176"><a href="marshaloptions-property-ado.md">スレッド</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-177">利用不可</span><span class="sxs-lookup"><span data-stu-id="e5df3-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-179">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-181">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-183">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-185">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-187">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="e5df3-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-188"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-189">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-190"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-191">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="e5df3-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e5df3-192">標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5df3-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5df3-193">メソッド</span><span class="sxs-lookup"><span data-stu-id="e5df3-193">Method</span></span></p></th>
<th><p><span data-ttu-id="e5df3-194">利用可能性</span><span class="sxs-lookup"><span data-stu-id="e5df3-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-196">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-197"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-198">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-200">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-202">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-204">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-206">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-207"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-208">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-210">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-211"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-212">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-214">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-216">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-218">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-220">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-222">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-224">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-226">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-227"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-228">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-229"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-230">はい</span><span class="sxs-lookup"><span data-stu-id="e5df3-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5df3-231"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-232">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5df3-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="e5df3-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e5df3-234">いいえ</span><span class="sxs-lookup"><span data-stu-id="e5df3-234">No</span></span></p></td>
</tr>
</tbody>
</table>

