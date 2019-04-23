---
title: permissionenum 列挙 (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287711"
---
# <a name="permissionenum-enumeration-dao"></a>permissionenum 列挙 (DAO)


**適用先:** Access 2013、Office 2013

" **Permissions**/権限" プロパティで、権限の種類を指定するために使用します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbseccreate</p></td>
<td><p>1-d</p></td>
<td><p>ユーザーは新しいドキュメントを作成できます (Document オブジェクトに対しては無効)。</p></td>
</tr>
<tr class="even">
<td><p>dbsecdbadmin</p></td>
<td><p>~</p></td>
<td><p>ユーザーはデータベースをレプリケートし、データベース パスワードを変更できます (Document オブジェクトに対しては無効)。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecdbcreate</p></td>
<td><p>1-d</p></td>
<td><p>ユーザーは新しいデータベースを作成できます。このオプションは、ワークグループ情報ファイル (Systen.mdw) の Databases コンテナーでのみ有効です。この定数は、Document オブジェクトに対しては無効です。</p></td>
</tr>
<tr class="even">
<td><p>dbsecdbexclusive</p></td>
<td><p>2/4</p></td>
<td><p>ユーザーはデータベースに排他的にアクセスできます。</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBOpen</p></td>
<td><p>pbm-2</p></td>
<td><p>ユーザーはデータベースを開くことができます。</p></td>
</tr>
<tr class="even">
<td><p>dbsecdelete</p></td>
<td><p>65536</p></td>
<td><p>ユーザーはオブジェクトを削除できます。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecdeletedata</p></td>
<td><p>128</p></td>
<td><p>ユーザーはレコードを削除できます。</p></td>
</tr>
<tr class="even">
<td><p>dbsecfullaccess</p></td>
<td><p>1048575</p></td>
<td><p>ユーザーはオブジェクトに完全にアクセスできます。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecinsertdata</p></td>
<td><p>32</p></td>
<td><p>ユーザーはレコードを追加できます。</p></td>
</tr>
<tr class="even">
<td><p>dbSecNoAccess</p></td>
<td><p>.0</p></td>
<td><p>ユーザーはオブジェクトにアクセスできません (Document オブジェクトに対しては無効)。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecreaddef</p></td>
<td><p>2/4</p></td>
<td><p>ユーザーは列情報およびインデックス情報を含むテーブル定義を読み取ることができます。</p></td>
</tr>
<tr class="even">
<td><p>dbsecreadsec</p></td>
<td><p>131072</p></td>
<td><p>ユーザーはオブジェクトのセキュリティ関連情報を読み取ることができます。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecreplacedata</p></td>
<td><p>64</p></td>
<td><p>ユーザーはレコードを変更できます。</p></td>
</tr>
<tr class="even">
<td><p>dbSecRetrieveData</p></td>
<td><p>1280</p></td>
<td><p>ユーザーは Document オブジェクトからデータを取得できます。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecwritedef</p></td>
<td><p>65548</p></td>
<td><p>ユーザーは列情報およびインデックス情報を含むテーブル定義を変更または削除できます。</p></td>
</tr>
<tr class="even">
<td><p>dbsecwriteowner</p></td>
<td><p>524288</p></td>
<td><p>ユーザーは "Owner/所有者" プロパティの設定を変更できます。</p></td>
</tr>
<tr class="odd">
<td><p>dbsecwritesec</p></td>
<td><p>262144</p></td>
<td><p>ユーザーはアクセス権限を変更できます。</p></td>
</tr>
</tbody>
</table>

