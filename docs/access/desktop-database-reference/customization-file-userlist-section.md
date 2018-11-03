---
title: カスタマイズ ファイルの UserList セクション
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62aaba79fa010de62fb1ac35939673b2056be3f7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944096"
---
# <a name="customization-file-userlist-section"></a>カスタマイズ ファイルの UserList セクション


**適用されます**Access 2013、Office 2013。

**Userlist**セクションは、同じセクション*の識別子*パラメーターを使用して、[**接続**] セクションに関係します。

このセクションでは、*ユーザー アクセス エントリ*を指定したユーザーのアクセス権を指定し、一致する [**接続**] セクションで*既定*の*アクセス エントリ*をオーバーライドを含めることができます。

## <a name="syntax"></a>構文

ユーザー アクセス エントリの形式は、次のとおりです。

*ユーザー名。 =*・ アクセス権。

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
<td><p>この接続を使用しているユーザーの<em>ユーザー名</em>です。 IIS<strong>サービス マネージャー</strong>のダイアログ ボックスは、有効なユーザー名が確立されます。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>・ アクセス権</em></strong></p></td>
<td><p>次のアクセス権のいずれかを指定します。
<br />
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

