---
title: "\"CopyDatabaseFile/データベースファイルのコピー\" マクロ アクション"
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b52644cb9a0a5140f45c42eaead84a63723c23e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479176"
---
# <a name="copydatabasefile-macro-action"></a>"CopyDatabaseFile/データベースファイルのコピー" マクロ アクション


**適用されます**Access 2013 |。Office 2013

" **CopyDatabaseFile/データベースファイルのコピー** " アクションを使用すると、Access プロジェクトに接続されている Microsoft SQL Server 7.0 以降のカレント データベースのコピーを作成できます。 アクセスでは、現在のデータベースをデタッチし、移行先サーバーに結び付けます。 データベースの切断と接続の詳細については、SQL Server のドキュメントを参照してください。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**データベースファイルのコピー**操作では、次の引数があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Database File Name/データベース ファイル名</strong></p></td>
<td><p>新しいマスター データ ファイルの名前を指定します。このファイルの既定のパスは、Access プロジェクト ファイル (.adp) の現在の場所です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Overwrite Existing File/既存ファイルの上書き</strong></p></td>
<td><p>同じ名前の既存のファイルを置換するかどうかを指定します。 場合<strong>[はい]</strong>に設定し、ファイル名が既に存在する、ファイルは上書きされます。 場合は<strong>No</strong>に設定ファイル名が既に存在する、ファイルが上書きされないと、アクションは失敗します。 ファイルが既に存在しない場合、この設定は無視されます。 既定値は [ <strong>はい</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Disconnect All Users/全ユーザーの切断</strong></p></td>
<td><p>データベースからユーザーを強制的かどうかを指定します。 場合は<strong>[はい]</strong>に設定、現在のデータベースに接続されているすべてのユーザーを切断し、データベースのコピー操作を続行できます。 場合設定<strong>なし</strong>もう 1 つまたはより多くのユーザーは、コピーのデータベース操作が失敗する、データベースに接続しています。 既定値は [ <strong>いいえ</strong>] です。</p>

> [!WARNING]
> <P>十分な通知を行わずにユーザーをデータベースから切断すると、データの損失を招く可能性があります。</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

コピー操作は同期操作であるため、データベースのコピーが完了するまで他の操作は実行できません。

**データベースファイルのコピー**操作は、データ、データ定義、およびデータベース オブジェクトをコピーするだけでなく、既定値、テキスト制約、ルックアップ値などの拡張プロパティもコピーします。

データベースのコピー操作の要件を次に示します。

  - データベース ファイルをコピーする前にすべてのアプリケーションとユーザーを切断する必要があります。

  - ナビゲーション ウィンドウ以外のすべてのオブジェクトとビューを閉じる必要があります。

  - カレント データベースはレプリケートできません。

  - サーバー データベースをコピーするには、ローカル コンピューターに Microsoft SQL Server Version 7.0 以降または SQL Server 2000 Desktop Engine が必要です。

<!-- end list -->

  - コピー元のサーバーにある SQL Server データベースは、単一のファイル データベースであることが必要です。

  - コピーを実行するユーザーは、コピー元とコピー先の両方の SQL Server コンピューターにおいて sysadmin ロールのメンバーである必要がありです。

モジュールの Visual Basic for Applications では、**データベースファイルのコピー**操作を実行するには、 **DoCmd**オブジェクトの**データベースファイルのコピー**メソッドを使用します。

