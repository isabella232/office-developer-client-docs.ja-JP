---
title: カスタマイズ ファイルの Connect セクション
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9455867ec47354a38084a67360d5ee7f3f66e874
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622502"
---
# <a name="customization-file-connect-section"></a>カスタマイズ ファイルの Connect セクション

**適用先**: Access 2013、Office 2013

ハンドラーの既定の動作では、すべての接続が拒否されます。 **connect** セクションで、この動作の例外を指定します。たとえば、 **connect** セクションが 1 つもないか、あっても空の場合、既定では接続は行われません。

**connect** セクションには、次のものを含めることができます。

- この接続で実行できる既定の読み取り/書き込み操作を指定する、既定のアクセス エントリ。このセクションに既定のアクセス エントリが存在しない場合、このセクションは無視されます。

- クライアントの接続文字列を置き換える新しい接続文字列。

## <a name="syntax"></a>構文

既定のアクセス エントリの形式は、次のとおりです。

`Access=accessRight`

置き換える接続文字列エントリの形式は、次のとおりです。

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Connect</strong></p></td>
<td><p>これが接続文字列のエントリであることを示すリテラル文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>クライアントのすべての接続文字列を置き換える文字列。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>これがアクセス エントリであることを示すリテラル文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRight</em></strong></p></td>
<td><p>次のアクセス権のいずれかを指定します。</p>
<p></p>
<ul>
<li><p><strong>NoAccess</strong> ユーザーは、データ ソースにアクセスできません。</p></li>
<li><p><strong>ReadOnly</strong> ユーザーは、データ ソースの読み取りが可能です。</p></li>
<li><p><strong>ReadWrite</strong> ユーザーは、データ ソースの読み取り/書き込みが可能です。</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


接続を許可する場合 (実際には、既定のハンドラー動作を無効にする) 場合は、[既定の接続] セクションのアクセス エントリをに設定し、他の接続識別子セクションを削除またはコメント *アウトします。*

