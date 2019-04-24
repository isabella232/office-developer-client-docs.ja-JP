---
title: Version プロパティ (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294653"
---
# <a name="databaseversion-property-dao"></a>Version プロパティ (DAO)

**適用先:** Access 2013、Office 2013

microsoft access ワークスペースでは、データベースを作成した microsoft Jet または microsoft access データベースエンジンの vesion を返します。 値の取得のみ可能な文字列型 (**String**) の値です。

## <a name="syntax"></a>構文

*式*。バージョン

*式***Database**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

戻り値は、次の書式設定のバージョン番号として評価される文字列型 (String) の値となります。

- Microsoft Access ワークスペースでは、このバージョン番号を "*major.minor*" という形式で表します。たとえば、"3.0"と表します。製品のバージョン番号は、バージョン番号 (3)、ピリオド、およびリリース番号 (0) から構成されます。

次の表は、Microsoft 製品の各種バージョンに搭載されているデータベース エンジンのバージョンの一覧です。

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>データベース エンジン</p></th>
<th><p>バージョン (リリース年)</p></th>
<th><p>Microsoft Access</p></th>
<th><p>Microsoft Visual Basic</p></th>
<th><p>Excel</p></th>
<th><p>Microsoft Visual C++</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>1.0 (1992)</p></td>
<td><p>1.0</p></td>
<td><p>該当なし</p></td>
<td><p>該当なし</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="even">
<td><p>Jet</p></td>
<td><p>1.1 (1993)</p></td>
<td><p>1.1</p></td>
<td><p>3.0</p></td>
<td><p>該当なし</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>2.0 (1994)</p></td>
<td><p>2.0</p></td>
<td><p>該当なし</p></td>
<td><p>該当なし</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="even">
<td><p>Jet</p></td>
<td><p>2.5 (1995)</p></td>
<td><p>該当なし</p></td>
<td><p>4.0 (16 ビット)</p></td>
<td><p>該当なし</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>3.0 (1995)</p></td>
<td><p>‘95 (7.0)</p></td>
<td><p>4.0 (32 ビット)</p></td>
<td><p>‘95 (7.0)</p></td>
<td><p>4.x</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>3.5 (1996)</p></td>
<td><p>‘97 (8.0)</p></td>
<td><p>5.0</p></td>
<td><p>‘97 (8.0)</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>4.0 (2000)</p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Access データベース エンジン</p></td>
<td><p>12.0 (2007)</p></td>
<td><p>2007</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

