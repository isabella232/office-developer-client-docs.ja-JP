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
# <a name="ado-error-reference"></a>ADO エラー リファレンス

**適用先:** Access 2013、Office 2013

**ErrorValueEnum** 定数は、ADO エラーの値を表します。これらの列挙定数をすべて記載した一覧 (値を含む) については、「 [付録 B: ADO エラー一覧](appendix-b-ado-errors.md)」を参照してください。このセクションでは、一部の注意が必要なエラーについて概説し、それが発生する可能性のある具体的な状況、または問題の解決策について説明します。 **ErrorValueEnum** 定数と正の 10 進値で表されるエラー番号の両方を示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>番号</p></th>
<th><p>ErrorValueEnum 定数</p></th>
<th><p>説明/考えられる原因</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>aderrproviderfailed</strong></p></td>
<td><p>プロバイダーが要求された操作を実行できませんでした。</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>間違った種類または許容範囲外の引数を使用しているか、使用している引数が競合しています。このエラーは、多くの場合、SQL SELECT ステートメント内の誤入力が原因で発生します。たとえば、フィールド名やテーブル名のスペルが間違っているときは、このエラーが生成される場合があります。このエラーは、SELECT ステートメント内のフィールド名やテーブル名がデータ ストアに存在しないときにも発生する場合があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>ファイルを開くことができませんでした。指定されたファイル名のスペルが間違っているか、ファイルが移動、名前変更、または削除されています。ネットワーク上のファイルの場合、ドライブが一時的に使用できない状態であるか、ネットワーク トラフィックの状態によってドライブに接続できない可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>aderrreadfile</strong></p></td>
<td><p>ファイルを読み込むことができませんでした。指定されたファイル名が間違っているか、ファイルが移動または削除されたか、ファイルが壊れている可能性があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>aderrwritefile</strong></p></td>
<td><p>ファイルへの書き込みに失敗しました。ファイルを閉じてから書き込もうとしたか、ファイルが壊れている可能性があります。ファイルがネットワーク ドライブ上にある場合は、ネットワークの一時的な状態によってネットワーク ドライブへの書き込みができない可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p><strong>BOF</strong> または <strong>EOF</strong> が True、または現在のレコードが削除されています。要求された操作には、現在のレコードが必要です。 <strong>Find</strong> または <strong>Seek</strong> を使用してレコード ポインターを所定のレコードに移動することにより、レコードを更新しようとしました。レコードが検出されない場合は、 <strong>EOF</strong> が True になります。このエラーは、 <strong>AddNew</strong> または <strong>Delete</strong> が失敗した後にも発生する場合があります。これらのメソッドが失敗したときには、現在のレコードが存在しないからです。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>このコンテキストで操作は許可されていません。</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>aderrcantchangeprovider</strong></p></td>
<td><p>指定されたプロバイダーが既に使用されているものと異なります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>aderrintransaction</strong></p></td>
<td><p>トランザクションの実行中に <strong>Connection</strong> オブジェクトを明示的に閉じることができません。現在トランザクションで使用されている <strong>Recordset</strong> オブジェクトまたは <strong>Connection</strong> オブジェクトは、閉じることができません。オブジェクトを閉じる前に、 <strong>RollbackTrans</strong> または <strong>CommitTrans</strong> を呼び出してください。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>オブジェクトまたはプロバイダーが、要求された操作を実行できません。一部の操作は特定のバージョンのプロバイダーでのみ実行できます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>要求された名前、または序数に対応する項目がコレクションで見つかりません。指定されたフィールド名またはテーブル名が間違っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>オブジェクトが既にコレクション内に存在しているため、追加できません。オブジェクトを同じコレクションに 2 回追加することはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>オブジェクトが無効になっています。</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>現在の操作に対して、アプリケーションが間違った型の値を使用しています。たとえば、ストリームを使用する必要のある操作で文字列を使用した場合などです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>オブジェクトが閉じている場合は、操作は許可されません。 <strong>Connection</strong> または <strong>Recordset</strong> が閉じています。たとえば、他のルーチンがグローバル オブジェクトを閉じた場合などです。このエラーは、操作を実行しようとする前に <strong>State</strong> プロパティを確認することによって防ぐことができます。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>オブジェクトが開いている場合は、操作は許可されません。開いているオブジェクトを開くことはできません。開いている <strong>Recordset</strong> にフィールドを追加することはできません。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>プロバイダーが見つかりません。正しくインストールされていない可能性があります。指定されたプロバイダー名が間違っているか、コードを実行するコンピューターに指定されたプロバイダーがインストールされていないか、インストールされたプロバイダーが壊れている可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>aderrboundtocommand</strong></p></td>
<td><p><strong>Command</strong> オブジェクトをソースとする <strong>Recordset</strong> オブジェクトの <strong>ActiveConnection</strong> プロパティを変更できません。アプリケーションが <strong>Command</strong> オブジェクトをソースとする <strong>Recordset</strong> に新しい <strong>Connection</strong> オブジェクトを適用しようとしました。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>aderrinvalidparaminfo</strong></p></td>
<td><p><strong>Parameter</strong> オブジェクトが適切に定義されていません。矛盾した、または不完全な情報が指定されました。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>aderrinvalidconnection</strong></p></td>
<td><p>この操作を実行するために接続を使用できません。このコンテキストで閉じているかあるいは無効です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>aderrnotreentrant</strong></p></td>
<td><p>イベント処理中に操作を行うことはできません。イベント ハンドラー内では、そのイベントを再度発生させる操作を実行できません。たとえば、ナビゲーション メソッドは <strong>WillMove</strong> イベント ハンドラーから呼び出さないようにする必要があります。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>非同期実行中に操作を行うことはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>ユーザーにより操作が取り消されました。アプリケーションが <strong>CancelUpdate</strong> メソッドまたは <strong>CancelBatch</strong> メソッドを呼び出し、現在の操作が取り消されました。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>非同期操作の保留中に、操作を行うことはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>aderrinvalidtransaction</strong></p></td>
<td><p>調整トランザクションが無効であるか、開始されていません。</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>aderrnotexecuting</strong></p></td>
<td><p>実行していない間に操作を行うことはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>aderrアン safeoperation</strong></p></td>
<td><p>このコンピューターの安全性の設定により、他のドメインのデータ ソースへのアクセスが禁止されています。</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adwrnsecuritydialog</strong></p></td>
<td><p>内部使用のために用意されています。使用しないでください (このエントリは完全性のために登録されています。このエラーがコードで発生することはありません)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adwrnsecuritydialogheader</strong></p></td>
<td><p>内部使用のために用意されています。使用しないでください (このエントリは完全性のために登録されています。このエラーがコードで発生することはありません)。</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>データ値がフィールドの整合性制約に反しています。 <strong>Field</strong> に新しい値を適用すると、キーが重複します。2 つのレコード間の関係の一方を形成する値は更新できません。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>aderrpermissiondenied</strong></p></td>
<td><p>権限が不十分なために、フィールドに書き込みができません。接続文字列で指定されたユーザーが、 <strong>Field</strong> に書き込むための適切な権限を保持していません。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>aderrdataoverflow</strong></p></td>
<td><p>データ値が大きすぎるために、フィールドのデータ型で表現できません。適用先のフィールドに大きすぎる数値が割り当てられました。たとえば、short 整数のフィールドに long 整数が割り当てられた場合などです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>aderrschemaviolation</strong></p></td>
<td><p>データ値がフィールドのデータ型と一致していないか、フィールドの制約に反しています。データ ストアに <strong>Field</strong> の値とは異なる検証制約があります。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>aderrsignmismatch</strong></p></td>
<td><p>データの値は符号付きですが、プロバイダーによって使用されるフィールド データ型は符号なしのため、変換に失敗しました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>aderrcantconvertvalue</strong></p></td>
<td><p>符号の不一致またはデータ オーバーフロー以外の理由により、データ値を変換できません。たとえば、変換によりデータの一部が切り捨てられる場合などです。</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>aderrcantcreate</strong></p></td>
<td><p>フィールドのデータ型が不明であったか、プロバイダーが操作を実行するのに十分なリソースを持っていなかったため、データ値を設定または取得できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>aderrcolumnnotonこの行</strong></p></td>
<td><p>レコードにこのフィールドが存在しません。指定されたフィールド名が間違っているか、現在のレコードの <strong>Fields</strong> コレクションには存在しないフィールド名が参照されました。  </p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>Either the source URL or the parent of the destination URL does not exist. There is a typographical error in either the source or destination URL. https://mysite/photos/myphoto.jpg代わりに、実際https://mysite/photo/myphoto.jpgにを使用する必要がある場合があります。 親 URL が誤入力されていることにより (この例では <em></em>photos ではなく <em></em>photo と指定したことにより) エラーが発生しています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>aderrtreepermissiondenied</strong></p></td>
<td><p>権限が不十分なために、ツリーまたはサブツリーにアクセスできません。接続文字列で指定されたユーザーが適切な権限を保持していません。</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>aderrinvalidurl</strong></p></td>
<td><p>URL に無効な文字が含まれています。URL が正しく入力されていることを確認してください。URL の前には、現在のプロバイダーに登録された接続体系が付加されます (たとえば、Internet Publishing Provider では http が登録されています)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>aderrresourcelocked</strong></p></td>
<td><p>指定された URL で表されるオブジェクトが、1 つ以上の他のプロセスによってロックされています。そのプロセスが終了するまで待機し、再度操作を試行してください。アクセスしようとしているオブジェクトは、他のユーザーまたはアプリケーションの他のプロセスによってロックされています。これはマルチユーザー環境で最も頻繁に発生します。</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>aderrresourceexists</strong></p></td>
<td><p>コピー操作を実行できません。宛先の URL で指定されたオブジェクトは既に存在します。 <strong>adCopyOverwrite</strong> を指定してオブジェクトを書き換えてください。ディレクトリ内のファイルをコピーするときに <strong>adCopyOverwrite</strong> を指定しない場合、コピー先の場所に既に存在する項目をコピーしようとすると、コピーが失敗します。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>サーバーが操作を完了できません。これは、サーバーが他の操作でビジー状態であるか、リソースが少なくなっていることが原因として考えられます。</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>aderrvolumenotfound</strong></p></td>
<td><p>プロバイダーが、URL で示された記憶装置の場所を特定できません。URL が正しく入力されていることを確認してください。記憶装置の URL が間違っている可能性がありますが、このエラーは他の原因でも発生します。装置がオフラインになっているか、ネットワーク トラフィックが混雑しているために、接続できない可能性があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>操作を実行できません。プロバイダーが十分な記憶域スペースを取得できません。サーバー上の一時ファイルを保存するための RAM またはハード ドライブのスペースが不足している可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>ソースまたは宛先の URL が、現在のレコードの範囲外です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>aderrunavailable 不可</strong></p></td>
<td><p>操作の完了に失敗し、状態は利用できません。フィールドが使用できないか操作が実行されなかった可能性があります。アクセスしようとしているフィールドを、他のユーザーが変更または削除した可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>この URL によって名前を付けられたレコードが存在しません。 <strong>Record</strong> オブジェクトを使用してファイルを開こうとしたときに、ファイル名またはファイルへのパスのスペルが誤って入力されました。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>削除するオブジェクトの URL が、現在のレコードの範囲外にあります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>aderrcatalognotset</strong></p></td>
<td><p>操作には有効な <strong>ParentCatalog</strong> が必要です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>接続が拒否されました。要求した新しい接続の特性が、既に使用されているものと異なります。</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>フィールドを更新できませんでした。詳細については、各フィールド オブジェクトの <strong>Status</strong> プロパティを確認してください。このエラーが発生する可能性のある状況は、データベースのレコードを変更または追加している途中で <strong>Field</strong> オブジェクトの値を変更した場合、または <strong>Field</strong> オブジェクト自体のプロパティを変更した場合の 2 つです。現在のレコードに含まれるフィールドの 1 つに存在する問題により、 <strong>Record</strong> または <strong>Recordset</strong> を更新できませんでした。 <strong>Fields</strong> コレクションを列挙し、各フィールドの <strong>Status</strong> プロパティを確認して、問題の原因を特定してください。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>プロバイダーが共有の制約をサポートしていません。ファイル共有を制限しようとしましたが、プロバイダーがその概念をサポートしていませんでした。</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>aderrdenytypenotsupported がサポートされている</strong></p></td>
<td><p>プロバイダーが、要求された種類の共有の制約をサポートしていません。プロバイダーがサポートしていない特定の種類のファイル共有制約を確立しようとしました。プロバイダーのドキュメントを参照して、サポートされているファイル共有制約を確認してください。</p></td>
</tr>
</tbody>
</table>

