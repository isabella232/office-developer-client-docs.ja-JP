---
title: "'TransferSQLDatabase/SQLデータベースの転送' マクロ アクション"
TOCTitle: TransferSQLDatabase Macro Action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 301fce8bcdeff45135c305054da72f4c75f503eb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476808"
---
# <a name="transfersqldatabase-macro-action"></a>"TransferSQLDatabase/SQLデータベースの転送" マクロ アクション


**適用されます**Access 2013 |。Office 2013

Access プロジェクトで、Microsoft SQL Server 7.0 以降のデータベースを別の SQL Server 7.0、またはそれ以降のデータベースを転送するのに**TransferSQLDatabase**アクションを使用できます。 データベースの転送の詳細については、SQL Server のマニュアルを参照してください。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**TransferSQLDatabase**アクションには、次の引数があります。

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
<td><p><strong>Server</strong></p></td>
<td><p>転送先の SQL Server 7.0 以降のデータベース サーバーの名前を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Database</strong></p></td>
<td><p>転送先のサーバーに作成される新しいデータベースの名前を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Use Trusted Connection/セキュリティ接続を使用する</strong></p></td>
<td><p>指定またはが存在しないかどうかは、SQL Server に信頼関係接続です。 場合は、信頼関係接続と<strong>ログイン名</strong>と<strong>パスワード</strong>の引数は必須ではありませんし、 <strong>[はい]</strong>に設定します。 <strong>いいえ</strong>、<strong>ログイン</strong>および<strong>パスワード</strong>の引数に設定が必要な場合です。 既定値は [ <strong>はい</strong>] です。 信頼関係接続を使用すると、SQL Server のセキュリティは、ネットワークとデータベースに 1 つのログを提供する Windows オペレーティング システムのセキュリティと統合します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Login/ログイン</strong></p></td>
<td><p>転送先のサーバーへのログイン名を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p><strong>ログイン</strong>引数のパスワード。 このパスワードは、Access プロジェクト内のテキストとして格納されますが、データベースの転送操作中に非表示。</p></td>
</tr>
<tr class="even">
<td><p><strong>Transfer Copy Data/データ コピーの転送</strong></p></td>
<td><p>データベースの転送処理にデータを含めるかどうかを指定します。[<strong>はい</strong>] に設定した場合は、すべてのテーブルのすべてのデータが、すべてのデータ構造、拡張プロパティ、およびデータベース オブジェクトと共に転送されます。[<strong>いいえ</strong>] に設定した場合は、テーブルのデータは含まれません。テーブル構造と拡張プロパティのみが、データベース ダイアグラムを除くその他すべてのデータベース オブジェクトと共に、転送先のサーバーに作成されます。既定値は [<strong>はい</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

データベースの転送中は、その他の操作を実行できません。

**TransferSQLDatabase**アクションでは、既定では、コピーのデータ、データ定義、データベース オブジェクト、および既定値、テキスト制約、ルックアップ値などの拡張プロパティです。

データベースを転送するには、次の要件があります。

  - 操作を実行するユーザーは、転送先のサーバーにおける sysadmin ロールのメンバーであること (転送元のサーバーでは特にロールは問いません)。

<!-- end list -->

  - Access プロジェクトに接続されている現在の SQL サーバーと、データベースの転送先のサーバーが SQL Server Version 7.0 以降であること。


> [!NOTE]
> <P>[!メモ] リンク サーバーは、データベースの転送時には転送されません。</P>



**TransferSQLDatabase**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**TransferSQLDatabase**メソッドを使用します。

