---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10af40231fc10e222f818896b3d65f44ac3d6d71
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477462"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="a0ea0-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span><span class="sxs-lookup"><span data-stu-id="a0ea0-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="a0ea0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0ea0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a0ea0-p101">Microsoft OLE DB Provider for Microsoft Indexing Service を使用すると、Microsoft インデックス サービスでインデックスを作成したファイル システムや Web データに対して、プログラムによる読み取り専用アクセスが可能になります。ADO アプリケーションでは、SQL クエリを使用してコンテンツおよびファイルのプロパティ情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-p101">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and Web data indexed by Microsoft Indexing Service. ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="a0ea0-106">このプロバイダーはフリースレッドであり、Unicode に対応しています。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="a0ea0-107">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="a0ea0-107">Connection String Parameters</span></span>

<span data-ttu-id="a0ea0-108">このプロバイダーに接続するには、**ConnectionString** プロパティの [Provider=](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="a0ea0-109">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="a0ea0-110">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="a0ea0-110">Typical Connection String</span></span>

<span data-ttu-id="a0ea0-111">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="a0ea0-112">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0ea0-113">キーワード</span><span class="sxs-lookup"><span data-stu-id="a0ea0-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="a0ea0-114">説明</span><span class="sxs-lookup"><span data-stu-id="a0ea0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="a0ea0-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-p102">OLE DB Provider for Microsoft Indexing Service を指定します。通常、この接続文字列ではこのキーワードのみを指定します。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-118"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="a0ea0-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-p103">インデックス サービスのカタログ名を指定します。このキーワードを指定しない場合は、既定のシステム カタログが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-121"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="a0ea0-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-p104">ユーザーの言語に関する設定を指定する一意の 32 ビット番号 (1033 など) を指定します。これらの設定は、日付と時刻の形式、アルファベット順の並べ替え方法、文字列の比較方法などを示します。このキーワードを指定しない場合は、既定のシステム ロケール識別子が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="a0ea0-125">コマンド テキスト</span><span class="sxs-lookup"><span data-stu-id="a0ea0-125">Command Text</span></span>

<span data-ttu-id="a0ea0-p105">インデックス サービスの SQL クエリの構文は、SQL-92 **SELECT** ステートメントおよびその **FROM** 句と **WHERE** 句の拡張機能で構成されます。クエリの結果は、OLE DB の行セットを通じて返され、ADO で利用して、 [Recordset](recordset-object-ado.md) オブジェクトとして操作できます。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="a0ea0-p106">正確に一致する語句の検索、ワイルドカードを使用したパターン検索や語幹検索を実行できます。検索ロジックでは、真偽判定、語の重要度、または他の語との類似性を基準にすることができます。"フリー テキスト" による検索も可能で、正確に一致する語ではなく、意味の一致するものを探すことができます。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="a0ea0-131">このプロバイダーはストアド プロシージャの呼び出しや単純なテーブル名 (たとえば、[CommandType](commandtype-property-ado.md) が常に **adCmdText** である場合など) を受け付けません。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="a0ea0-132">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="a0ea0-132">Recordset Behavior</span></span>

<span data-ttu-id="a0ea0-133">次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="a0ea0-134">静的カーソルの種類 (**adOpenStatic**) のみがあります。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="a0ea0-135">プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 [Recordset](properties-collection-ado.md) の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="a0ea0-136">標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0ea0-137">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-137">Property</span></span></p></th>
<th><p><span data-ttu-id="a0ea0-138">利用可能性</span><span class="sxs-lookup"><span data-stu-id="a0ea0-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-140">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-142">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-144">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-146">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-147"><a href="bookmark-property-ado.md">ブックマーク</a>\*</span><span class="sxs-lookup"><span data-stu-id="a0ea0-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="a0ea0-148">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-150">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-152">常に <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="a0ea0-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-153"><a href="cursortype-property-ado.md">カーソル。</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-154">常に <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="a0ea0-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-156">常に <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="a0ea0-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-158">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-159"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-160">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-161"><a href="locktype-property-ado.md">ロック。</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-162">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-163"><a href="marshaloptions-property-ado.md">スレッド</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-164">利用不可</span><span class="sxs-lookup"><span data-stu-id="a0ea0-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-166">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-168">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-170">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-172">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-173"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-174">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a0ea0-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-175"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-176">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-177"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-178">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0ea0-179">\*ブックマークは**レコード セット**上に存在するこの機能のためにプロバイダーを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="a0ea0-180">標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0ea0-181">メソッド</span><span class="sxs-lookup"><span data-stu-id="a0ea0-181">Method</span></span></p></th>
<th><p><span data-ttu-id="a0ea0-182">利用可能性</span><span class="sxs-lookup"><span data-stu-id="a0ea0-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-184">いいえ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-185"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-186">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-188">いいえ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-190">いいえ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-192">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-194">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-195"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-196">いいえ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-197"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-198">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-199"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-200">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-202">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-204">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-206">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-207"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-208">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-209"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-210">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-211"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-212">はい</span><span class="sxs-lookup"><span data-stu-id="a0ea0-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ea0-213"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ea0-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="a0ea0-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a0ea0-216">いいえ</span><span class="sxs-lookup"><span data-stu-id="a0ea0-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a0ea0-217">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0ea0-217">See also</span></span>

<span data-ttu-id="a0ea0-218">特定の実装の詳細と機能については、Microsoft OLE DB プロバイダーが Microsoft インデックス サービスでは、Microsoft OLE DB プログラマ リファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0ea0-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

