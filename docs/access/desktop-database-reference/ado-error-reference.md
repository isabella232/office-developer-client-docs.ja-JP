---
title: ADO エラー リファレンス
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283395"
---
# <a name="ado-error-reference"></a><span data-ttu-id="dbbd6-102">ADO エラー リファレンス</span><span class="sxs-lookup"><span data-stu-id="dbbd6-102">ADO error reference</span></span>

<span data-ttu-id="dbbd6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbbd6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbbd6-p101">**ErrorValueEnum** 定数は、ADO エラーの値を表します。これらの列挙定数をすべて記載した一覧 (値を含む) については、「 [付録 B: ADO エラー一覧](appendix-b-ado-errors.md)」を参照してください。このセクションでは、一部の注意が必要なエラーについて概説し、それが発生する可能性のある具体的な状況、または問題の解決策について説明します。 **ErrorValueEnum** 定数と正の 10 進値で表されるエラー番号の両方を示します。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p101">The **ErrorValueEnum** constant describes the ADO error values. For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md). This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem. Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbbd6-108">番号</span><span class="sxs-lookup"><span data-stu-id="dbbd6-108">Number</span></span></p></th>
<th><p><span data-ttu-id="dbbd6-109">ErrorValueEnum 定数</span><span class="sxs-lookup"><span data-stu-id="dbbd6-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="dbbd6-110">説明/考えられる原因</span><span class="sxs-lookup"><span data-stu-id="dbbd6-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-112"><strong>aderrproviderfailed</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-113">プロバイダーが要求された操作を実行できませんでした。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p102">間違った種類または許容範囲外の引数を使用しているか、使用している引数が競合しています。このエラーは、多くの場合、SQL SELECT ステートメント内の誤入力が原因で発生します。たとえば、フィールド名やテーブル名のスペルが間違っているときは、このエラーが生成される場合があります。このエラーは、SELECT ステートメント内のフィールド名やテーブル名がデータ ストアに存在しないときにも発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p102">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another. This error is often caused by a typographical error in an SQL SELECT statement. For example, a misspelled field name or table name can generate this error. This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p103">ファイルを開くことができませんでした。指定されたファイル名のスペルが間違っているか、ファイルが移動、名前変更、または削除されています。ネットワーク上のファイルの場合、ドライブが一時的に使用できない状態であるか、ネットワーク トラフィックの状態によってドライブに接続できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p103">File could not be opened. A misspelled file name was specified, or a file has been moved, renamed, or deleted. Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-126"><strong>aderrreadfile</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p104">ファイルを読み込むことができませんでした。指定されたファイル名が間違っているか、ファイルが移動または削除されたか、ファイルが壊れている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p104">File could not be read. The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-130"><strong>aderrwritefile</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p105">ファイルへの書き込みに失敗しました。ファイルを閉じてから書き込もうとしたか、ファイルが壊れている可能性があります。ファイルがネットワーク ドライブ上にある場合は、ネットワークの一時的な状態によってネットワーク ドライブへの書き込みができない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p105">Write to file failed. You might have closed a file and then tried to write to it, or the file might be corrupted. If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p106"><strong>BOF</strong> または <strong>EOF</strong> が True、または現在のレコードが削除されています。要求された操作には、現在のレコードが必要です。 <strong>Find</strong> または <strong>Seek</strong> を使用してレコード ポインターを所定のレコードに移動することにより、レコードを更新しようとしました。レコードが検出されない場合は、 <strong>EOF</strong> が True になります。このエラーは、 <strong>AddNew</strong> または <strong>Delete</strong> が失敗した後にも発生する場合があります。これらのメソッドが失敗したときには、現在のレコードが存在しないからです。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p106">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record. An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record. If the record is not found, <strong>EOF</strong> will be True. This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-143">このコンテキストで操作は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-145"><strong>aderrcantchangeprovider</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-146">指定されたプロバイダーが既に使用されているものと異なります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-148"><strong>aderrintransaction</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p107">トランザクションの実行中に <strong>Connection</strong> オブジェクトを明示的に閉じることができません。現在トランザクションで使用されている <strong>Recordset</strong> オブジェクトまたは <strong>Connection</strong> オブジェクトは、閉じることができません。オブジェクトを閉じる前に、 <strong>RollbackTrans</strong> または <strong>CommitTrans</strong> を呼び出してください。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p107"><strong>Connection</strong> object cannot be explicitly closed while in a transaction. A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed. Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p108">オブジェクトまたはプロバイダーが、要求された操作を実行できません。一部の操作は特定のバージョンのプロバイダーでのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p108">The object or provider is not capable of performing the requested operation. Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p109">要求された名前、または序数に対応する項目がコレクションで見つかりません。指定されたフィールド名またはテーブル名が間違っています。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p109">Item cannot be found in the collection corresponding to the requested name or ordinal. An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p110">オブジェクトが既にコレクション内に存在しているため、追加できません。オブジェクトを同じコレクションに 2 回追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p110">Object is already in collection. Cannot append. An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-167">オブジェクトが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p111">現在の操作に対して、アプリケーションが間違った型の値を使用しています。たとえば、ストリームを使用する必要のある操作で文字列を使用した場合などです。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p111">Application uses a value of the wrong type for the current operation. You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p112">オブジェクトが閉じている場合は、操作は許可されません。 <strong>Connection</strong> または <strong>Recordset</strong> が閉じています。たとえば、他のルーチンがグローバル オブジェクトを閉じた場合などです。このエラーは、操作を実行しようとする前に <strong>State</strong> プロパティを確認することによって防ぐことができます。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p112">Operation is not allowed when the object is closed. The <strong>Connection</strong> or <strong>Recordset</strong> has been closed. For example, some other routine might have closed a global object. You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p113">オブジェクトが開いている場合は、操作は許可されません。開いているオブジェクトを開くことはできません。開いている <strong>Recordset</strong> にフィールドを追加することはできません。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p113">Operation is not allowed when the object is open. An object that is open cannot be opened. Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p114">プロバイダーが見つかりません。正しくインストールされていない可能性があります。指定されたプロバイダー名が間違っているか、コードを実行するコンピューターに指定されたプロバイダーがインストールされていないか、インストールされたプロバイダーが壊れている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p114">Provider cannot be found. It may not be properly installed. The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-189"><strong>aderrboundtocommand</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p115"><strong>Command</strong> オブジェクトをソースとする <strong>Recordset</strong> オブジェクトの <strong>ActiveConnection</strong> プロパティを変更できません。アプリケーションが <strong>Command</strong> オブジェクトをソースとする <strong>Recordset</strong> に新しい <strong>Connection</strong> オブジェクトを適用しようとしました。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p115">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed. The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-193"><strong>aderrinvalidparaminfo</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p116"><strong>Parameter</strong> オブジェクトが適切に定義されていません。矛盾した、または不完全な情報が指定されました。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p116"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-197"><strong>aderrinvalidconnection</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p117">この操作を実行するために接続を使用できません。このコンテキストで閉じているかあるいは無効です。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p117">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-201"><strong>aderrnotreentrant</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p118">イベント処理中に操作を行うことはできません。イベント ハンドラー内では、そのイベントを再度発生させる操作を実行できません。たとえば、ナビゲーション メソッドは <strong>WillMove</strong> イベント ハンドラーから呼び出さないようにする必要があります。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p118">Operation cannot be performed while processing event. An operation cannot be performed within an event handler that causes the event to fire again. For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-207">非同期実行中に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p119">ユーザーにより操作が取り消されました。アプリケーションが <strong>CancelUpdate</strong> メソッドまたは <strong>CancelBatch</strong> メソッドを呼び出し、現在の操作が取り消されました。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p119">Operation has been canceled by the user. The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-214">非同期操作の保留中に、操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-216"><strong>aderrinvalidtransaction</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-217">調整トランザクションが無効であるか、開始されていません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-219"><strong>aderrnotexecuting</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-220">実行していない間に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-222"><strong>aderrアン safeoperation</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-223">このコンピューターの安全性の設定により、他のドメインのデータ ソースへのアクセスが禁止されています。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-225"><strong>adwrnsecuritydialog</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p120">内部使用のために用意されています。使用しないでください (このエントリは完全性のために登録されています。このエラーがコードで発生することはありません)。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p120">For internal use only. Don't use. (Entry was included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-231"><strong>adwrnsecuritydialogheader</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p121">内部使用のために用意されています。使用しないでください (このエントリは完全性のために登録されています。このエラーがコードで発生することはありません)。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p121">For internal use only. Don't use. (Entry included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p122">データ値がフィールドの整合性制約に反しています。 <strong>Field</strong> に新しい値を適用すると、キーが重複します。2 つのレコード間の関係の一方を形成する値は更新できません。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p122">Data value conflicts with the integrity constraints of the field. A new value for a <strong>Field</strong> would cause a duplicate key. A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-242"><strong>aderrpermissiondenied</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p123">権限が不十分なために、フィールドに書き込みができません。接続文字列で指定されたユーザーが、 <strong>Field</strong> に書き込むための適切な権限を保持していません。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p123">Insufficient permission prevents writing to the field. The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-246"><strong>aderrdataoverflow</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p124">データ値が大きすぎるために、フィールドのデータ型で表現できません。適用先のフィールドに大きすぎる数値が割り当てられました。たとえば、short 整数のフィールドに long 整数が割り当てられた場合などです。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p124">Data value is too large to be represented by the field data type. A numeric value that is too large for the intended field was assigned. For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-251"><strong>aderrschemaviolation</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p125">データ値がフィールドのデータ型と一致していないか、フィールドの制約に反しています。データ ストアに <strong>Field</strong> の値とは異なる検証制約があります。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p125">Data value conflicts with the data type or constraints of the field. The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-255"><strong>aderrsignmismatch</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-256">データの値は符号付きですが、プロバイダーによって使用されるフィールド データ型は符号なしのため、変換に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-258"><strong>aderrcantconvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p126">符号の不一致またはデータ オーバーフロー以外の理由により、データ値を変換できません。たとえば、変換によりデータの一部が切り捨てられる場合などです。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p126">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-262"><strong>aderrcantcreate</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-263">フィールドのデータ型が不明であったか、プロバイダーが操作を実行するのに十分なリソースを持っていなかったため、データ値を設定または取得できません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-265"><strong>aderrcolumnnotonこの行</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p127">レコードにこのフィールドが存在しません。指定されたフィールド名が間違っているか、現在のレコードの <strong>Fields</strong> コレクションには存在しないフィールド名が参照されました。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p127">Record does not contain this field. An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-270">Either the source URL or the parent of the destination URL does not exist.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="dbbd6-271">There is a typographical error in either the source or destination URL.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="dbbd6-272">https://mysite/photos/myphoto.jpg代わりに、実際https://mysite/photo/myphoto.jpgにを使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="dbbd6-273">親 URL が誤入力されていることにより (この例では <em></em>photos ではなく <em></em>photo と指定したことにより) エラーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-275"><strong>aderrtreepermissiondenied</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p129">権限が不十分なために、ツリーまたはサブツリーにアクセスできません。接続文字列で指定されたユーザーが適切な権限を保持していません。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p129">Permissions are insufficient to access tree or subtree. The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-279"><strong>aderrinvalidurl</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p130">URL に無効な文字が含まれています。URL が正しく入力されていることを確認してください。URL の前には、現在のプロバイダーに登録された接続体系が付加されます (たとえば、Internet Publishing Provider では http が登録されています)。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p130">URL contains invalid characters. Make sure the URL is typed correctly. The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-284"><strong>aderrresourcelocked</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p131">指定された URL で表されるオブジェクトが、1 つ以上の他のプロセスによってロックされています。そのプロセスが終了するまで待機し、再度操作を試行してください。アクセスしようとしているオブジェクトは、他のユーザーまたはアプリケーションの他のプロセスによってロックされています。これはマルチユーザー環境で最も頻繁に発生します。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p131">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again. The object you are trying to access has been locked by another user or by another process in your application. This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-290"><strong>aderrresourceexists</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p132">コピー操作を実行できません。宛先の URL で指定されたオブジェクトは既に存在します。 <strong>adCopyOverwrite</strong> を指定してオブジェクトを書き換えてください。ディレクトリ内のファイルをコピーするときに <strong>adCopyOverwrite</strong> を指定しない場合、コピー先の場所に既に存在する項目をコピーしようとすると、コピーが失敗します。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p132">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object. If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p133">サーバーが操作を完了できません。これは、サーバーが他の操作でビジー状態であるか、リソースが少なくなっていることが原因として考えられます。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p133">The server cannot complete the operation. This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-300"><strong>aderrvolumenotfound</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p134">プロバイダーが、URL で示された記憶装置の場所を特定できません。URL が正しく入力されていることを確認してください。記憶装置の URL が間違っている可能性がありますが、このエラーは他の原因でも発生します。装置がオフラインになっているか、ネットワーク トラフィックが混雑しているために、接続できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p134">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly. The URL of the storage device might be incorrect, but this error can occur for other reasons. The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p135">操作を実行できません。プロバイダーが十分な記憶域スペースを取得できません。サーバー上の一時ファイルを保存するための RAM またはハード ドライブのスペースが不足している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p135">Operation cannot be performed. Provider cannot obtain enough storage space. There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-312">ソースまたは宛先の URL が、現在のレコードの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-314"><strong>aderrunavailable 不可</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p136">操作の完了に失敗し、状態は利用できません。フィールドが使用できないか操作が実行されなかった可能性があります。アクセスしようとしているフィールドを、他のユーザーが変更または削除した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p136">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted. Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p137">この URL によって名前を付けられたレコードが存在しません。 <strong>Record</strong> オブジェクトを使用してファイルを開こうとしたときに、ファイル名またはファイルへのパスのスペルが誤って入力されました。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p137">Record named by this URL does not exist. While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-324">削除するオブジェクトの URL が、現在のレコードの範囲外にあります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-326"><strong>aderrcatalognotset</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-327">操作には有効な <strong>ParentCatalog</strong> が必要です。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p138">接続が拒否されました。要求した新しい接続の特性が、既に使用されているものと異なります。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p138">Connection was denied. The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p139">フィールドを更新できませんでした。詳細については、各フィールド オブジェクトの <strong>Status</strong> プロパティを確認してください。このエラーが発生する可能性のある状況は、データベースのレコードを変更または追加している途中で <strong>Field</strong> オブジェクトの値を変更した場合、または <strong>Field</strong> オブジェクト自体のプロパティを変更した場合の 2 つです。現在のレコードに含まれるフィールドの 1 つに存在する問題により、 <strong>Record</strong> または <strong>Recordset</strong> を更新できませんでした。 <strong>Fields</strong> コレクションを列挙し、各フィールドの <strong>Status</strong> プロパティを確認して、問題の原因を特定してください。  </span><span class="sxs-lookup"><span data-stu-id="dbbd6-p139">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects. This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself. The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record. Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbbd6-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p140">プロバイダーが共有の制約をサポートしていません。ファイル共有を制限しようとしましたが、プロバイダーがその概念をサポートしていませんでした。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p140">Provider does not support sharing restrictions. An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbbd6-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-344"><strong>aderrdenytypenotsupported がサポートされている</strong></span><span class="sxs-lookup"><span data-stu-id="dbbd6-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="dbbd6-p141">プロバイダーが、要求された種類の共有の制約をサポートしていません。プロバイダーがサポートしていない特定の種類のファイル共有制約を確立しようとしました。プロバイダーのドキュメントを参照して、サポートされているファイル共有制約を確認してください。</span><span class="sxs-lookup"><span data-stu-id="dbbd6-p141">Provider does not support the requested kind of sharing restriction. An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider. See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

