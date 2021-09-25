---
title: TransferSQLDatabase マクロ アクション
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 645dc3b4f098be2cd3f758c216c5606dff3ba9b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593433"
---
# <a name="transfersqldatabase-macro-action"></a>TransferSQLDatabase マクロ アクション

**適用先**: Access 2013、Office 2013

In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database. データベースの転送の詳細については、次のドキュメントSQL Serverしてください。

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。

## <a name="setting"></a>Setting

"TransferSQLDatabase/SQLデータベースの転送" アクションの引数は次のとおりです。

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
<td><p><strong>サーバー</strong></p></td>
<td><p>転送先の SQL Server 7.0 以降のデータベース サーバーの名前を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>データベース</strong></p></td>
<td><p>転送先のサーバーに作成される新しいデータベースの名前を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Use Trusted Connection/セキュリティ接続を使用する</strong></p></td>
<td><p>アプリケーションへの信頼できる接続が確立されているかどうかを指定SQL Server。 [はい <strong>] に設定</strong>すると、信頼できる接続が確立され <strong>、Login</strong> 引数と <strong>Password</strong> 引数は必要ありません。 [いいえ]<strong>に設定すると</strong><strong>、Login 引数と</strong> <strong>Password</strong>引数が必要になります。 既定値は [ <strong>はい</strong>] です。 信頼できる接続を使用する場合、SQL Server セキュリティは Windows オペレーティング システム のセキュリティと統合され、ネットワークとデータベースに 1 つのログオンを提供します。</p></td>
</tr>
<tr class="even">
<td><p><strong>ログイン</strong></p></td>
<td><p>転送先のサーバーへのログイン名を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>"Login/ログイン" 引数のパスワードを指定します。このパスワードは Access プロジェクトにテキストとして格納されますが、データベースの転送処理中は表示されません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Transfer Copy Data/データ コピーの転送</strong></p></td>
<td><p>データベースの転送処理にデータを含めるかどうかを指定します。[<strong>はい</strong>] に設定した場合は、すべてのテーブルのすべてのデータが、すべてのデータ構造、拡張プロパティ、およびデータベース オブジェクトと共に転送されます。[<strong>いいえ</strong>] に設定した場合は、テーブルのデータは含まれません。テーブル構造と拡張プロパティのみが、データベース ダイアグラムを除くその他すべてのデータベース オブジェクトと共に、転送先のサーバーに作成されます。既定値は [<strong>はい</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

データベースの転送中は、その他の操作を実行できません。

The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.

データベースを転送するには、次の要件があります。

- 操作を実行するユーザーは、転送先のサーバーにおける sysadmin ロールのメンバーであること (転送元のサーバーでは特にロールは問いません)。

- Access プロジェクトに接続されている現在の SQL サーバーと、データベースの転送先のサーバーが SQL Server Version 7.0 以降であること。

  > [!NOTE]
  > [!メモ] リンク サーバーは、データベースの転送時には転送されません。

To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.

