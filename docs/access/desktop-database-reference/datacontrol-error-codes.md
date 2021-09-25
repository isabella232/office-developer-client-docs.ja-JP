---
title: DataControl のエラー コード
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8fde92fc77ce53f265ab62e1c6334d919a81e722
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565556"
---
# <a name="datacontrol-error-codes"></a>DataControl のエラー コード


**適用先:** Access 2013、Office 2013

次の表は、[RDS.DataControl](datacontrol-object-rds.md) オブジェクトのエラー コードの一覧です。下位 2 バイトを正の 10 進数に変換した値、エラー コード全体を負の 10 進数に変換した値、および 16 進数値を示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>RDS.DataControl エラー コード</p></th>
<th><p>番号</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>IDS_AsyncPending</strong></p></td>
<td><p>4107<br />
-2146824175<br />
0x800A1011</p></td>
<td><p>非同期操作の保留中に、操作を行うことはできません。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_BadInlineTablegram</strong></p></td>
<td><p>4105<br />
-2146824183<br />
0x800A1009</p></td>
<td><p>インライン テーブルグラムが正しくありません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantConnect</strong></p></td>
<td><p>4099<br />
-2146824189<br />
0x800A1003</p></td>
<td><p>サーバーに接続できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantCreateObject</strong></p></td>
<td><p>4100<br />
-2146824188<br />
0x800A1004</p></td>
<td><p>ビジネス オブジェクトは作成できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantFindDataspace</strong></p></td>
<td><p>4102<br />
-2146824186<br />
0x800A1006</p></td>
<td><p>Dataspace プロパティは無効です。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantInvokeMethod</strong></p></td>
<td><p>4101<br />
-2146824187<br />
0x800A1005</p></td>
<td><p>ビジネス オブジェクトのメソッドを呼び出せません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CrossDomainWarning</strong></p></td>
<td><p>4112<br />
-2146824170<br />
0x800A1016</p></td>
<td><p>このページは別のドメインにあるデータにアクセスします。 このアクセスを許可してもよろしいですか? このメッセージをInternet Explorer、セキュリティで保護された Web サイトを [インターネット オプション] ダイアログ<strong></strong>ボックスの [セキュリティ] タブの [信頼済みサイト]<strong>領域に</strong>追加できます。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidADCClientVersion</strong></p></td>
<td><p>4106<br />
-2146824176<br />
0x800A1010</p></td>
<td><p>無効な RDS クライアント バージョン : クライアントがサーバーより新しい。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_INVALIDARG</strong></p></td>
<td><p>5376<br />
-2147019520<br />
0x80071500</p></td>
<td><p>いくつかの引数は無効です。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidBindings</strong></p></td>
<td><p>4097<br />
-2146824191<br />
0x800A1001</p></td>
<td><p>プロパティのバインド エラーです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_InvalidParam</strong></p></td>
<td><p>4110<br />
-2146824172<br />
0x800A1014</p></td>
<td><p>いくつかの引数は無効です。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_NOINTERFACE</strong></p></td>
<td><p>5377<br />
-2147019519<br />
0x80071501</p></td>
<td><p>そのインターフェイスはサポートされていません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_NotReentrant</strong></p></td>
<td><p>4111<br />
-2146824171<br />
0x800A1015</p></td>
<td><p>イベント ハンドラーの処理中に要求を実行することはできません。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ObjectNotSafe</strong></p></td>
<td><p>4103<br />
-2146824185<br />
0x800A1007</p></td>
<td><p>このコンピューターの安全性の設定により、ビジネス オブジェクトの作成が禁止されています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RecordsetNotOpen</strong></p></td>
<td><p>4109<br />
-2146824173<br />
0x800A1013</p></td>
<td><p>レコードセット (<strong>Recordset</strong>) が開かれていません。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ResetInvalidField</strong></p></td>
<td><p>4108<br />
-2146824174<br />
0x800A1012</p></td>
<td><p><strong>SortColumn</strong> または <strong>FilterColumn</strong> に指定された列は存在しません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RowsetNotUpdateable</strong></p></td>
<td><p>4104<br />
-2146824184<br />
0x800A1008</p></td>
<td><p>行セットは更新できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_UnexpectedError</strong></p></td>
<td><p>4351<br />
-2146823937<br />
0x800A10FF</p></td>
<td><p>予期しないエラーが発生しました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_UpdatesFailed</strong></p></td>
<td><p>4098<br />
-2146824190<br />
0x800A1002</p></td>
<td><p>データベースを更新できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_URLMONNotFound</strong></p></td>
<td><p>4119<br />
-2146824169<br />
0x800A1017</p></td>
<td><p>DataControl <strong>URL</strong> プロパティにはシステム ファイル Urlmon.dll が必要ですが、ファイルが見つかりません。</p></td>
</tr>
</tbody>
</table>

