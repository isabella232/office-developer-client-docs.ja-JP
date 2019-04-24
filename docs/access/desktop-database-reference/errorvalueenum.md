---
title: errorvalueenum (Access デスクトップデータベースリファレンス)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293323"
---
# <a name="errorvalueenum"></a>ErrorValueEnum

**適用先:** Access 2013、Office 2013

ADO 実行時エラーの種類を表します。

エラー番号には次の 3 種類の形式があります。

- 正の 10 進値: 10 進数で表された完全エラー番号の下位 2 バイト。この数値は、Visual Basic の既定のエラー メッセージ ダイアログ ボックスに表示されます。たとえば、実行時エラー '3707' がその例です。

- 負の 10 進値: 完全エラー番号を 10 進数に変換したもの。

- 16 進値: 完全エラー番号の 16 進数表記。 Windows 機能コードは 4 桁目です。 ADO エラー番号のファシリティコードは *、* です。例: 0x800***A***0e7b。

> [!NOTE]
> OLE DB エラーが ADO アプリケーションに渡される場合があります。 通常、これらは Windows ファシリティコード*4*で識別できます。 たとえば、0x800_**4**_....これらの番号の詳細については、「 *OLE DB プログラマリファレンス*」の「16章」を参照してください。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>aderrboundtocommand</strong></p></td>
<td><p>3707<br />
-2146824581<br />
0x800A0E7B</p></td>
<td><p><strong>Command</strong> オブジェクトをソースに持つ <strong>Recordset</strong> オブジェクトの <strong>ActiveConnection</strong> プロパティを変更できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>3732<br />
-2146824556<br />
0x800A0E94</p></td>
<td><p>サーバーは操作を完了できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>3748<br />
-2146824540<br />
0x800A0EA4</p></td>
<td><p>接続が拒否されました。 要求された新規接続の特性が現在使用中の特性と異なります。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrcantchangeprovider</strong></p></td>
<td><p>3220<br />
-2146825068<br />
0x800a0c94</p></td>
<td><p>指定されたプロバイダーが既に使用されているものと異なります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrcantconvertvalue</strong></p></td>
<td><p>3724<br />
-2146824564<br />
0x800A0E8C</p></td>
<td><p>符号の不一致またはデータ オーバーフロー以外の理由により、データ値を変換できません。 たとえば、変換によりデータの一部が切り捨てられる場合などです。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrcantcreate</strong></p></td>
<td><p>3725<br />
-2146824563<br />
0x800A0E8D</p></td>
<td><p>フィールドのデータ型が不明であったか、プロバイダーが操作を実行するのに十分なリソースを持っていなかったため、データ値を設定または取得できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrcatalognotset</strong></p></td>
<td><p>3747<br />
-2146824541<br />
0x800A0EA3</p></td>
<td><p>操作には有効な <strong>ParentCatalog</strong> が必要です。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrcolumnnotonこの行</strong></p></td>
<td><p>3726<br />
-2146824562<br />
0x800A0E8E</p></td>
<td><p>レコードにこのフィールドが存在しません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>3421<br />
-2146824867<br />
0x800A0D5D</p></td>
<td><p>現在の操作に対して、間違った型の値を使用しています。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrdataoverflow</strong></p></td>
<td><p>3721<br />
-2146824567<br />
0x800A0E89</p></td>
<td><p>データ値が大きすぎるために、フィールドのデータ型で表現できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>3738<br />
-2146824550<br />
0x800A0E9A</p></td>
<td><p>削除されるオブジェクトの URL は現在のレコードの範囲外です。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>3750<br />
-2146824538<br />
0x800A0EA6</p></td>
<td><p>プロバイダーが共有の制約をサポートしていません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrdenytypenotsupported がサポートされている</strong></p></td>
<td><p>3751<br />
-2146824537<br />
0x800A0EA7</p></td>
<td><p>プロバイダーが、要求された種類の共有の制約をサポートしていません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>3251<br />
-2146825037<br />
0x800A0CB3</p></td>
<td><p>オブジェクトまたはプロバイダーは要求された操作を実行できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>3749<br />
-2146824539<br />
0x800A0EA5</p></td>
<td><p>フィールドを更新できませんでした。 詳細については、各 Field オブジェクトの <strong>Status</strong> プロパティを参照してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>3219<br />
-2146825069<br />
0x800a0c93</p></td>
<td><p>このコンテキストで操作は許可されていません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>3719<br />
-2146824569<br />
0x800A0E87</p></td>
<td><p>データの値がフィールドの整合性制約に反しています。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrintransaction</strong></p></td>
<td><p>3246<br />
-2146825042<br />
0x800A0CAE</p></td>
<td><p>トランザクションの実行中に <strong>Connection</strong> オブジェクトを明示的に閉じることができません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>3001<br />
-2146825287<br />
0x800A0BB9</p></td>
<td><p>間違った種類または許容範囲外の引数を使用しているか、使用している引数が競合しています。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrinvalidconnection</strong></p></td>
<td><p>3709<br />
-2146824579<br />
0x800A0E7D</p></td>
<td><p>この操作を実行するために接続を使用できません。 このコンテキストで閉じているかあるいは無効です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrinvalidparaminfo</strong></p></td>
<td><p>3708<br />
-2146824580<br />
0x800A0E7C</p></td>
<td><p><strong>Parameter</strong> オブジェクトが適切に定義されていません。 矛盾した、または不完全な情報が指定されました。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrinvalidtransaction</strong></p></td>
<td><p>3714<br />
-2146824574<br />
0x800A0E82</p></td>
<td><p>調整トランザクションが無効であるか、開始されていません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrinvalidurl</strong></p></td>
<td><p>3729<br />
-2146824559<br />
0x800A0E91</p></td>
<td><p>URL に無効な文字が含まれています。 URL が正しく入力されているか確認してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>3265<br />
-2146825023<br />
0x800A0CC1</p></td>
<td><p>要求された名前、または序数に対応する項目がコレクションで見つかりません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>3021<br />
-2146825267<br />
0x800A0BCD</p></td>
<td><p><strong>BOF</strong> または <strong>EOF</strong> が True であるか、現在のレコードが削除されています。 要求された操作には現在のレコードが必要です。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrnotexecuting</strong></p></td>
<td><p>3715<br />
-2146824573<br />
0x800A0E83</p></td>
<td><p>実行していない間に操作を行うことはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrnotreentrant</strong></p></td>
<td><p>3710<br />
-2146824578<br />
0x800A0E7E</p></td>
<td><p>イベント処理中に操作を行うことはできません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>3704<br />
-2146824584<br />
0x800A0E78</p></td>
<td><p>オブジェクトが閉じている場合は、操作は許可されません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>3367<br />
-2146824921<br />
0x800A0D27</p></td>
<td><p>オブジェクトは既にコレクションに存在します。 追加できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>3420<br />
-2146824868<br />
0x800A0D5C</p></td>
<td><p>オブジェクトが無効になっています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>3705<br />
-2146824583<br />
0x800A0E79</p></td>
<td><p>オブジェクトが開いている場合は、操作は許可されません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>3002<br />
-2146825286<br />
0x800A0BBA</p></td>
<td><p>ファイルを開くことができませんでした。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>3712<br />
-2146824576<br />
0x800A0E80</p></td>
<td><p>ユーザーにより操作が取り消されました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>3734<br />
-2146824554<br />
0x800A0E96</p></td>
<td><p>操作を実行できません。 プロバイダーによって十分な記憶域が確保できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrpermissiondenied</strong></p></td>
<td><p>3720<br />
-2146824568<br />
0x800A0E88</p></td>
<td><p>権限不足のためフィールドの書き込みはできません。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrproviderfailed</strong></p></td>
<td><p>3000<br />
-2146825288<br />
0x800A0BB8</p></td>
<td><p>プロバイダーが要求された操作を実行できませんでした。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>3706<br />
-2146824582<br />
0x800A0E7A</p></td>
<td><p>プロバイダーが見つかりません。 正しくインストールされていない可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrreadfile</strong></p></td>
<td><p>3003<br />
-2146825285<br />
0x800A0BBB</p></td>
<td><p>ファイルを読み込むことができませんでした。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrresourceexists</strong></p></td>
<td><p>3731<br />
-2146824557<br />
0x800A0E93</p></td>
<td><p>コピー操作を実行できません。 宛先の URL で指定されたオブジェクトは既に存在します。 オブジェクトを置き換えるためには <strong>adCopyOverwrite</strong> を指定してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrresourcelocked</strong></p></td>
<td><p>3730<br />
-2146824558<br />
0x800A0E92</p></td>
<td><p>指定された URL によって表されたオブジェクトは 1 つ以上の他のプロセスによってロックされています。プロセスが終了するまで待って、操作を再度実行してください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>3735<br />
-2146824553<br />
0x800A0E97</p></td>
<td><p>ソースまたは宛先の URL が、現在のレコードの範囲外です。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrschemaviolation</strong></p></td>
<td><p>3722<br />
-2146824566<br />
0x800A0E8A</p></td>
<td><p>データ値がフィールドのデータ型と一致していないか、フィールドの制約に反しています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrsignmismatch</strong></p></td>
<td><p>3723<br />
-2146824565<br />
0x800A0E8B</p></td>
<td><p>データの値は符号付きですが、プロバイダーによって使用されるフィールド データ型は符号なしのため、変換に失敗しました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>3713<br />
-2146824575<br />
0x800A0E81</p></td>
<td><p>非同期操作の保留中に、操作を行うことはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>3711<br />
-2146824577<br />
0x800A0E7F</p></td>
<td><p>非同期実行中に操作を行うことはできません。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrtreepermissiondenied</strong></p></td>
<td><p>3728<br />
-2146824560<br />
0x800A0E90</p></td>
<td><p>権限が不十分なために、ツリーまたはサブツリーにアクセスできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrunavailable 不可</strong></p></td>
<td><p>3736<br />
-2146824552<br />
0x800A0E98</p></td>
<td><p>操作の完了に失敗し、状態は利用できません。 フィールドが利用できないか、操作が実行されなかった可能性があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrアン safeoperation</strong></p></td>
<td><p>3716<br />
-2146824572<br />
0x800A0E84</p></td>
<td><p>このコンピューターの安全性の設定により、他のドメインのデータ ソースへのアクセスが禁止されています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>3727<br />
-2146824561<br />
0x800A0E8F</p></td>
<td><p>ソース URL または宛先の URL の親が存在しません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>3737<br />
-2146824551<br />
0x800A0E99</p></td>
<td><p>この URL によって名前を付けられたレコードが存在しません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>aderrvolumenotfound</strong></p></td>
<td><p>3733<br />
-2146824555<br />
0x800A0E95</p></td>
<td><p>プロバイダーが、URL で示された記憶装置の場所を特定できません。 URL が正しく入力されているか確認してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderrwritefile</strong></p></td>
<td><p>3004<br />
-2146825284<br />
0x800A0BBC</p></td>
<td><p>ファイルへの書き込みに失敗しました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adwrnsecuritydialog</strong></p></td>
<td><p>3717<br />
-2146824571<br />
0x800A0E85</p></td>
<td><p>内部使用のために用意されています。 使用しないでください。</p></td>
</tr>
<tr class="even">
<td><p><strong>adwrnsecuritydialogheader</strong></p></td>
<td><p>3718<br />
-2146824570<br />
0x800A0E86</p></td>
<td><p>内部使用のために用意されています。 使用しないでください。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

パッケージ: **com.ms.wfc.data**

次の ADO/WFC 等価のサブセットのみを定義します。

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums tocommand を指定します。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums DATACONVERSION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums FEATURENOTAVAILABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums ILLEGALOPERATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums を指定します。 intransaction</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums INVALIDARGUMENT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums connection。 invalidconnection</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の値を取得します。 invalidparaminfo</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums ITEMNOTFOUND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums NOCURRENTRECORD</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の実行</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。 notreentrant</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums closed。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums/オブジェクトのコレクション</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の値がありません。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums ado</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums が取り消されました</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums PROVIDERNOTFOUND</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums STILLCONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums STILLEXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の取り消し操作</p></td>
</tr>
</tbody>
</table>

