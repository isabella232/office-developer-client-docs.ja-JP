---
title: カスタマイズ ファイルの UserList セクション
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295157"
---
# <a name="customization-file-userlist-section"></a>カスタマイズ ファイルの UserList セクション


**適用先:** Access 2013、Office 2013

**userlist** セクションは、同じセクションの *identifier* パラメーターによって、**connect** セクションと関連付けられています。

このセクションには、指定されたユーザーのアクセス権を指定する*ユーザーアクセスエントリ*を含めることができます。また、一致する**connect**セクションの*既定*の*アクセスエントリ*を上書きします。

## <a name="syntax"></a>構文

ユーザー アクセス エントリの形式は、次のとおりです。

*userName * * * =* accessrights * * *

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
<td><p><em>userName</em></p></td>
<td><p>この接続を使用しているユーザーの "ユーザー名"。 有効なユーザー名は IIS の [サービス マネージャー] ダイアログ ボックスで設定されます。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>次のアクセス権のいずれかを指定します。<br />
</p>
<ul>
<li><p><strong>NoAccess</strong> ユーザーは、データ ソースにアクセスできません。</p></li>
<li><p><strong>ReadOnly</strong> ユーザーは、データ ソースの読み取りが可能です。</p></li>
<li><p><strong>ReadWrite</strong> ユーザーは、データ ソースの読み取り/書き込みが可能です。</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

