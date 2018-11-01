---
title: カスタマイズ ファイルの UserList セクション
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4aa7604edc887e97cbdfbea9b75e6f46ad55f35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880769"
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

