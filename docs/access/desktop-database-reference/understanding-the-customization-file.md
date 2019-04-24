---
title: カスタマイズ ファイルの概要
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314071"
---
# <a name="understanding-the-customization-file"></a>カスタマイズ ファイルの概要


**適用先:** Access 2013、Office 2013

カスタマイズファイルの各セクションヘッダーは、type と parameter を**\[** 含む角かっこ () で構成されています。 4つのセクションの種類は、リテラル文字列**connect**、 **sql**、 **userlist**、または**logs**で示されます。 パラメーターは、リテラル文字列、既定値、ユーザー指定の識別子、または何も指定されていません。

つまり、各セクションは以下のセクション ヘッダーのいずれかで示されます。

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

セクション ヘッダーには以下の要素があります。

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
<td><p><strong>結び付ける</strong></p></td>
<td><p>接続文字列を変更するリテラル文字列です。</p></td>
</tr>
<tr class="even">
<td><p><strong>sql</strong></p></td>
<td><p>コマンド文字列を変更するリテラル文字列です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>userlist</strong></p></td>
<td><p>特定のユーザーのアクセス権を変更するリテラル文字列です。</p></td>
</tr>
<tr class="even">
<td><p><strong>ログ</strong></p></td>
<td><p>操作エラーを記録するログ ファイルを指定するリテラル文字列です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>default</strong></p></td>
<td><p>識別子が指定されていない場合、または検出されない場合に使用されるリテラル文字列です。</p></td>
</tr>
<tr class="even">
<td><p><em>識別子</em></p></td>
<td><p>"接続" 文字列または "コマンド" 文字列内の文字列と一致する文字列です。</p>
<p></p>
<ul>
<li><p>セクション ヘッダーに <strong>connect</strong> があり、識別子の文字列が接続文字列内にある場合は、connect セクションが使用されます。</p></li>
<li><p>セクション ヘッダーに <strong>sql</strong> があり、識別子の文字列がコマンド文字列内にある場合は、sql セクションが使用されます。</p></li>
<li><p>セクション ヘッダーに <strong>userlist</strong> があり、識別子の文字列が <strong>connect</strong> セクションの識別子と一致する場合は、userlist セクションが使用されます。</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


**DataFactory** はハンドラーを呼び出し、クライアントのパラメーターを渡します。ハンドラーは、クライアント パラメーター内の文字列全体を対象として、該当するセクション ヘッダー内の識別子と一致する文字列を検索します。一致する文字列が見つかると、そのセクションの内容がクライアント パラメーターに適用されます。

各セクションは次の状況下で使用されます。

  - connect **** セクションは、クライアントの connect 文字列キーワードの値の部分が "**Data Source = * * * value*" で、 **connect**セクションの識別子と一致する場合に使用され*ます。*

  - **sql** セクションは、クライアントのコマンド文字列が **sql** セクションの識別子と一致する文字列を含んでいる場合に使用されます。

  - 一致する識別子が存在しない場合は、既定のパラメーターを持つ **connect** セクションまたは **sql** セクションが使用されます。

  - **userlist** セクションは、 **userlist** セクションの識別子が **connect** セクションの識別子と一致する場合に使用されます。一致する場合は、 **userlist** セクションの内容が、 **connect** セクションによって管理される接続に適用されます。

  - 接続文字列またはコマンド文字列中の文字列がどの **connect** セクション ヘッダーまたは **sql** セクション ヘッダーの識別子とも一致せず、また、既定のパラメーターを持つ **connect** セクション ヘッダーまたは **sql** セクション ヘッダーがない場合は、クライアント文字列がそのまま使用されます。

  - **logs** セクションは、 **DataFactory** の動作中に常に使用されます。

