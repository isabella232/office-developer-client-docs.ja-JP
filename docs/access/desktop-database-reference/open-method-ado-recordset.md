---
title: Open メソッド (ADO Recordset)
TOCTitle: Open Method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6887770c8e0c3b98b6ff990c884c5325d6ce6d3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479074"
---
# <a name="open-method-ado-recordset"></a><span data-ttu-id="0b283-102">Open メソッド (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="0b283-102">Open Method (ADO Recordset)</span></span>


<span data-ttu-id="0b283-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b283-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="0b283-104">カーソルを開きます。</span><span class="sxs-lookup"><span data-stu-id="0b283-104">Opens a cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b283-105">構文</span><span class="sxs-lookup"><span data-stu-id="0b283-105">Syntax</span></span>

<span data-ttu-id="0b283-106">*レコード セット*です。*ソース*、 *ActiveConnection*、 *CursorType*、 *LockType*、*オプション*を開く</span><span class="sxs-lookup"><span data-stu-id="0b283-106">*recordset*.Open*Source*, *ActiveConnection*, *CursorType*, *LockType*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="0b283-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b283-107">Parameters</span></span>

  - <span data-ttu-id="0b283-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="0b283-108">*Source*</span></span>

  - <span data-ttu-id="0b283-p101">省略可能です。有効な **Command** オブジェクト、SQL ステートメント、テーブル名、ストアド プロシージャの呼び出し、URL、または永続的に保存された [Recordset](command-object-ado.md) を格納しているファイル名や [Stream](stream-object-ado.md) オブジェクト名に評価されるバリアント型 ( [Variant](recordset-object-ado.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b283-p101">Optional. A **Variant** that evaluates to a valid [Command](command-object-ado.md) object, an SQL statement, a table name, a stored procedure call, a URL, or the name of a file or [Stream](stream-object-ado.md) object containing a persistently stored [Recordset](recordset-object-ado.md).</span></span>

  - <span data-ttu-id="0b283-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="0b283-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="0b283-p102">省略可能です。有効な **Connection** オブジェクトのオブジェクト変数名に評価されるバリアント型 ( [Variant](connection-object-ado.md) ) の値、または **ConnectionString** パラメーターを含む文字列型 ( [String](connectionstring-property-ado.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b283-p102">Optional. Either a **Variant** that evaluates to a valid [Connection](connection-object-ado.md) object variable name, or a **String** that contains [ConnectionString](connectionstring-property-ado.md) parameters.</span></span>

  - <span data-ttu-id="0b283-114">*カーソル。*</span><span class="sxs-lookup"><span data-stu-id="0b283-114">*CursorType*</span></span>

  - <span data-ttu-id="0b283-p103">省略可能です。プロバイダーが [Recordset](cursortypeenum.md) を開くときに使用するカーソルの種類を決める **CursorTypeEnum** 値を指定します。既定値は **adOpenForwardOnly** です。</span><span class="sxs-lookup"><span data-stu-id="0b283-p103">Optional. A [CursorTypeEnum](cursortypeenum.md) value that determines the type of cursor that the provider should use when opening the **Recordset**. The default value is **adOpenForwardOnly**.</span></span>

  - <span data-ttu-id="0b283-118">*ロック。*</span><span class="sxs-lookup"><span data-stu-id="0b283-118">*LockType*</span></span>

  - <span data-ttu-id="0b283-p104">省略可能です。プロバイダーが [Recordset](locktypeenum.md) を開くときに使用するロック (同時作用) の種類を決めるための **LockTypeEnum** 値を指定します。既定値は **adLockReadOnly** です。</span><span class="sxs-lookup"><span data-stu-id="0b283-p104">Optional. A [LockTypeEnum](locktypeenum.md) value that determines what type of locking (concurrency) the provider should use when opening the **Recordset**. The default value is **adLockReadOnly**.</span></span>

  - <span data-ttu-id="0b283-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="0b283-122">*Options*</span></span>

  - <span data-ttu-id="0b283-123">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="0b283-123">Optional.</span></span> <span data-ttu-id="0b283-124">プロバイダーする必要があります評価方法*元*の引数以外の**コマンド**オブジェクトを表す、または**レコード セット**は、それ以前に保存したファイルから復元するかを示す**Long**値。</span><span class="sxs-lookup"><span data-stu-id="0b283-124">A **Long** value that indicates how the provider should evaluate the *Source* argument if it represents something other than a **Command** object, or that the **Recordset** should be restored from a file where it was previously saved.</span></span> <span data-ttu-id="0b283-125">1 つまたは複数[CommandTypeEnum](commandtypeenum.md)または[ExecuteOptionEnum](executeoptionenum.md)の値をビットごとの AND 演算子で組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="0b283-125">Can be one or more [CommandTypeEnum](commandtypeenum.md) or [ExecuteOptionEnum](executeoptionenum.md) values, which can be combined with a bitwise AND operator.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0b283-126">[!メモ] 永続化された <STRONG>Recordset</STRONG> を含む <STRONG>Stream</STRONG> から <STRONG>Recordset</STRONG> を開く場合、 <STRONG>ExecuteOptionEnum</STRONG> 値の <STRONG>adAsyncFetchNonBlocking</STRONG> を使用しても無効です。この場合、フェッチは同期であり、ブロッキングが行われます。</span><span class="sxs-lookup"><span data-stu-id="0b283-126">If you open a <STRONG>Recordset</STRONG> from a <STRONG>Stream</STRONG> containing a persisted <STRONG>Recordset</STRONG>, using an <STRONG>ExecuteOptionEnum</STRONG> value of <STRONG>adAsyncFetchNonBlocking</STRONG> will not have an effect; the fetch will be synchronous and blocking.</span></span></P>



<span data-ttu-id="0b283-127">**Open** メソッドを使用する場合は、 **ExecuteOpenEnum** に **adExecuteNoRecords** または **adExecuteStream** を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="0b283-127">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Open**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b283-128">解説</span><span class="sxs-lookup"><span data-stu-id="0b283-128">Remarks</span></span>

<span data-ttu-id="0b283-129">ADO の **Recordset** の既定のカーソルは、サーバー側にある読み取り専用の前方スクロール カーソルです。</span><span class="sxs-lookup"><span data-stu-id="0b283-129">The default cursor for an ADO **Recordset** is a forward-only, read-only cursor located on the server.</span></span>

<span data-ttu-id="0b283-130">**Recordset** オブジェクトで **Open** メソッドを使用すると、ベース テーブルからのレコード、クエリの結果、または以前に保存された **Recordset** を表すカーソルを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="0b283-130">Using the **Open** method on a **Recordset** object opens a cursor that represents records from a base table, the results of a query, or a previously saved **Recordset**.</span></span>

<span data-ttu-id="0b283-131">オプションの*Source*引数を使用して、次のいずれかを使用してデータ ソースを指定する:**コマンド**オブジェクト変数、SQL ステートメント、ストアド プロシージャ、テーブル名、URL やファイルの完全なパス名です。</span><span class="sxs-lookup"><span data-stu-id="0b283-131">Use the optional *Source* argument to specify a data source using one of the following: a **Command** object variable, an SQL statement, a stored procedure, a table name, a URL, or a complete file path name.</span></span> <span data-ttu-id="0b283-132">*ソース*がファイルのパス名の場合は、ことができます、完全なパス ("c:\\dir\\file.rst")、相対パス ("..\\file.rst")、または URL ("https://files/file.rst")。</span><span class="sxs-lookup"><span data-stu-id="0b283-132">If *Source* is a file path name, it can be a full path ("c:\\dir\\file.rst"), a relative path ("..\\file.rst"), or a URL ("https://files/file.rst").</span></span>

<span data-ttu-id="0b283-133">ありません、呼び出しが成功したかどうかを判断する簡単な方法がないため、レコードを返さないアクション クエリを実行するのには**Open**メソッドの*Source*引数を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0b283-133">It is not a good idea to use the *Source* argument of the **Open** method to perform an action query that doesnt return records because there is no easy way to determine whether the call succeeded.</span></span> <span data-ttu-id="0b283-134">このようなクエリによって返される**レコード セット**は閉じられます。</span><span class="sxs-lookup"><span data-stu-id="0b283-134">The **Recordset** returned by such a query will be closed.</span></span> <span data-ttu-id="0b283-135">SQL INSERT ステートメントなど、レコードを返さないクエリを実行するのには、 **Command**オブジェクトの[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))メソッドまたは**Connection**オブジェクトの[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\))メソッドを代わりに呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0b283-135">Call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method of a **Command** object or the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method of a **Connection** object instead to perform a query that, such as a SQL INSERT statement, that doesnt return records.</span></span>

<span data-ttu-id="0b283-136">*暗黙的*では、 [ActiveConnection](activeconnection-property-ado.md)プロパティに対応し、接続を開くには、**レコード セット**オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="0b283-136">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado.md) property and specifies in which connection to open the **Recordset** object.</span></span> <span data-ttu-id="0b283-137">この引数に接続の定義を指定すると、ADO により、指定されたパラメーターを使用して新しい接続が開かれます。</span><span class="sxs-lookup"><span data-stu-id="0b283-137">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="0b283-138">クライアント側カーソルで**レコード セット**を開いた後 (**CursorLocation** = **adUseClient**)、別のプロバイダーに更新を送信するには、このプロパティの値を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="0b283-138">After opening the **Recordset** with a client-side cursor (**CursorLocation** = **adUseClient**), you can change the value of this property to send updates to another provider.</span></span> <span data-ttu-id="0b283-139">また、このプロパティを **Nothing** (Microsoft Visual Basic の場合) または NULL に設定すると、その **Recordset** を任意のプロバイダーから切断することができます。</span><span class="sxs-lookup"><span data-stu-id="0b283-139">Or you can set this property to **Nothing** (in Microsoft Visual Basic) or NULL to disconnect the **Recordset** from any provider.</span></span> <span data-ttu-id="0b283-140">ただし、サーバー側カーソルの **ActiveConnection** を変更すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0b283-140">Changing **ActiveConnection** for a server-side cursor generates an error, however.</span></span>

<span data-ttu-id="0b283-141">**Recordset** オブジェクトのプロパティに直接対応するその他の引数 (*Source*、*CursorType*、および *LockType*) と、プロパティの関係は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0b283-141">For the other arguments that correspond directly to properties of a **Recordset** object (*Source*, *CursorType*, and *LockType*), the relationship of the arguments to the properties is as follows:</span></span>

  - <span data-ttu-id="0b283-142">**Recordset** オブジェクトを開く前のプロパティは、読み取り/書き込み可能です。</span><span class="sxs-lookup"><span data-stu-id="0b283-142">The property is read/write before the **Recordset** object is opened.</span></span>

  - <span data-ttu-id="0b283-p109">**Open** メソッドの実行時に、対応する引数を指定しないと、プロパティの設定値が使用されます。引数を指定した場合は、対応するプロパティの設定値が上書きされて引数の値に更新されます。</span><span class="sxs-lookup"><span data-stu-id="0b283-p109">The property settings are used unless you pass the corresponding arguments when executing the **Open** method. If you pass an argument, it overrides the corresponding property setting, and the property setting is updated with the argument value.</span></span>

  - <span data-ttu-id="0b283-145">**Recordset** オブジェクトを開いた後、プロパティは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="0b283-145">After you open the **Recordset** object, these properties become read-only.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0b283-146">[!メモ] <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Source</STRONG> プロパティに有効な <A href="source-property-ado-recordset.md">Command</A> オブジェクトが設定されている場合、その <STRONG>Recordset</STRONG> オブジェクトが開いていなくても、 <STRONG>ActiveConnection</STRONG> プロパティは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="0b283-146">The <STRONG>ActiveConnection</STRONG> property is read only for <STRONG>Recordset</STRONG> objects whose <A href="source-property-ado-recordset.md">Source</A> property is set to a valid <STRONG>Command</STRONG> object, even if the <STRONG>Recordset</STRONG> object isn't open.</span></span></P>



<span data-ttu-id="0b283-147">*変換元*の引数で、**コマンド**オブジェクトを渡すし *、暗黙的*にも合格すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0b283-147">If you pass a **Command** object in the *Source* argument and also pass an *ActiveConnection* argument, an error occurs.</span></span> <span data-ttu-id="0b283-148">**Command** オブジェクトの **ActiveConnection** プロパティは、あらかじめ有効な **Connection** オブジェクトまたは接続文字列に設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b283-148">The **ActiveConnection** property of the **Command** object must already be set to a valid **Connection** object or connection string.</span></span>

<span data-ttu-id="0b283-149">*Source*引数に**Command**オブジェクト以外の値を渡すと場合、は、*変換元*の引数の評価を最適化するために*オプション*の引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b283-149">If you pass something other than a **Command** object in the *Source* argument, you can use the *Options* argument to optimize evaluation of the *Source* argument.</span></span> <span data-ttu-id="0b283-150">*Options*引数が定義されていない場合は、ADO プロバイダーの呼び出しかどうか、引数は、SQL ステートメント、ストアド プロシージャ、URL、またはテーブル名を決定する必要があるためパフォーマンスが低下が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b283-150">If the *Options* argument is not defined, you may experience diminished performance because ADO must make calls to the provider to determine if the argument is an SQL statement, a stored procedure, a URL, or a table name.</span></span> <span data-ttu-id="0b283-151">どのような*ソース*の種類がわかっている場合を使用している、関連するコードに直接ジャンプするのには ADO を指示する*オプション*引数を設定します。</span><span class="sxs-lookup"><span data-stu-id="0b283-151">If you know what *Source* type you're using, setting the *Options* argument instructs ADO to jump directly to the relevant code.</span></span> <span data-ttu-id="0b283-152">*オプション*の引数では、*変換元*の型は一致しない、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0b283-152">If the *Options* argument does not match the *Source* type, an error occurs.</span></span>

<span data-ttu-id="0b283-153">場合は*変換元*の引数に**Stream**オブジェクトを渡すと、他の引数に情報を渡さないでください。</span><span class="sxs-lookup"><span data-stu-id="0b283-153">If you pass a **Stream** object in the *Source* argument, you should not pass information into the other arguments.</span></span> <span data-ttu-id="0b283-154">そのようにすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0b283-154">Doing so will generate an error.</span></span> <span data-ttu-id="0b283-155">**Stream** から **Recordset** を開く場合は、 **ActiveConnection** の情報は保持されません。</span><span class="sxs-lookup"><span data-stu-id="0b283-155">The **ActiveConnection** information is not retained when a **Recordset** is opened from a **Stream**.</span></span>

<span data-ttu-id="0b283-156">*オプション*引数の既定値は**adCmdFile** **レコード セット**に関連付けられている接続が存在しない場合です。</span><span class="sxs-lookup"><span data-stu-id="0b283-156">The default for the *Options* argument is **adCmdFile** if no connection is associated with the **Recordset**.</span></span> <span data-ttu-id="0b283-157">代表的な例では、永続的に保存された **Recordset** オブジェクトの場合がこれに該当します。</span><span class="sxs-lookup"><span data-stu-id="0b283-157">This will typically be the case for persistently stored **Recordset** objects.</span></span>

<span data-ttu-id="0b283-p114">データ ソースがレコードを返さない場合、プロバイダーは [BOF](bof-eof-properties-ado.md) プロパティと [EOF](bof-eof-properties-ado.md) プロパティを **True** に設定し、カレント レコードの位置が未定義になります。カーソルの種類によっては、この空の **Recordset** オブジェクトに新しいデータを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="0b283-p114">If the data source returns no records, the provider sets both the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties to **True**, and the current record position is undefined. You can still add new data to this empty **Recordset** object if the cursor type allows it.</span></span>

<span data-ttu-id="0b283-p115">開いている **Recordset** に対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して、関連するシステム リソースをすべて解放します。オブジェクトを閉じてもメモリからは削除されないので、そのオブジェクトのプロパティを変更したり、**Open** メソッドを使用してもう一度開いたりすることができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。</span><span class="sxs-lookup"><span data-stu-id="0b283-p115">When you have concluded your operations over an open **Recordset** object, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="0b283-163">**ActiveConnection**プロパティを設定すると、前に**Open**を呼び出す**レコード セット**の[Fields](fields-collection-ado.md)コレクションにフィールドを追加することによって作成した**レコード セット**のインスタンスを作成するのにはオペランドが無い。</span><span class="sxs-lookup"><span data-stu-id="0b283-163">Before the **ActiveConnection** property is set, call **Open** with no operands to create an instance of a **Recordset** created by appending fields to the **Recordset** [Fields](fields-collection-ado.md) collection.</span></span>

<span data-ttu-id="0b283-164">[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定している場合は、非同期に行を取得できる方法が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="0b283-164">If you have set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**, you can retrieve rows asynchronously in one of two ways.</span></span> <span data-ttu-id="0b283-165">\**AdAsyncFetch\*\*\*オプション*を設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0b283-165">The recommended method is to set *Options* to **adAsyncFetch**.</span></span> <span data-ttu-id="0b283-166">もう 1 つの方法として、 [Properties](properties-collection-ado.md) コレクションで "非同期行セット処理" ダイナミック プロパティを使用することもできますが、 **Options** パラメーターを **adAsyncFetch** に設定していない場合は、関連して取得されたイベントが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b283-166">Alternatively, you can use the "Asynchronous Rowset Processing" dynamic property in the [Properties](properties-collection-ado.md) collection, but related retrieved events can be lost if you do not set the **Options** parameter to **adAsyncFetch**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0b283-167">MS Remote プロバイダーでバック グラウンドのフェッチは、 <STRONG>Open</STRONG>メソッドの<EM>Options</EM>パラメーターでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0b283-167">Background fetching in the MS Remote provider is supported only through the <STRONG>Open</STRONG> method's <EM>Options</EM> parameter.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="0b283-p117">[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b283-p117">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


