---
title: カスタマイズ ファイルの UserList セクション
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9da8cac1450e8ce1d7def2ed9049bdfe53e0f626
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558570"
---
# <a name="customization-file-userlist-section"></a>カスタマイズ ファイルの UserList セクション


**適用先:** Access 2013、Office 2013

**userlist** セクションは、同じセクションの *identifier* パラメーターによって、**connect** セクションと関連付けられています。

このセクションには、指定 *したユーザー* のアクセス権を指定し、一致する接続セクションの既定のアクセス エントリを上書きするユーザー アクセス エントリを **含** めできます。

## <a name="syntax"></a>構文

ユーザー アクセス エントリの形式は、次のとおりです。

*userName***=* accessRights***

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
<td><p>この接続を使用しているユーザーの "ユーザー名"。有効なユーザー名は IIS の [サービス マネージャー] ダイアログ ボックスで設定されます。</p></td>
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

