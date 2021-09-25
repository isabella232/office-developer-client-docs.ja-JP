---
title: CopyDatabaseFile マクロ アクション
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 44f079d84ec3b651b114ed9341fbf5361caf87e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615733"
---
# <a name="copydatabasefile-macro-action"></a>CopyDatabaseFile マクロ アクション

**適用先**: Access 2013、Office 2013

" **CopyDatabaseFile/データベースファイルのコピー** " アクションを使用すると、Access プロジェクトに接続されている Microsoft SQL Server 7.0 以降のカレント データベースのコピーを作成できます。 Access は、現在のデータベースをデタッチし、コピー先サーバーに接続します。 データベースの切断と接続の詳細については、SQL Server のドキュメントを参照してください。

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 


## <a name="setting"></a>Setting

"CopyDatabaseFile/データベースファイルのコピー" アクションの引数は次のとおりです。

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
<td><p>既存のファイルを同じ名前のファイルで置き換えるかどうかを指定します。[はい] に設定した場合に、同じ名前のファイルが既に存在すると、ファイルは上書きされます。[いいえ] に設定した場合、同じ名前のファイルが既に存在すると、ファイルは上書きされず、アクションは失敗します。同じ名前のファイルが存在しない場合、この設定は無視されます。既定値は [はい] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Disconnect All Users/全ユーザーの切断</strong></p></td>
<td><p>ユーザーを強制的にデータベースから切断するかどうかを指定します。[はい] に設定した場合は、カレント データベースに接続されているすべてのユーザーを切断し、データベースのコピー操作を進めることができます。[いいえ] に設定した場合は、データベースに接続しているユーザーが 1 人でもいると、データベースのコピー操作は失敗します。既定値は [いいえ] です。 



</p><p><strong>警告</strong>: 適切な警告なしにデータベースからユーザーを切断すると、データが失われる可能性があります。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

コピー操作は同期操作であるため、データベースのコピーが完了するまで他の操作は実行できません。

The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.

データベースのコピー操作の要件を次に示します。

- データベース ファイルをコピーする前にすべてのアプリケーションとユーザーを切断する必要があります。

- ナビゲーション ウィンドウ以外のすべてのオブジェクトとビューを閉じる必要があります。

- カレント データベースはレプリケートできません。

- サーバー データベースをコピーするには、ローカル コンピューターに Microsoft SQL Server Version 7.0 以降または SQL Server 2000 Desktop Engine が必要です。

- コピー元のサーバーにある SQL Server データベースは、単一のファイル データベースであることが必要です。

- コピーを実行するユーザーは、コピー元とコピー先の両方の SQL Server コンピューターにおいて sysadmin ロールのメンバーである必要がありです。

To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.

