---
title: Connection.CreateQueryDef メソッド (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6f54768e9c6297fb9e0d129f9545f88aaad8cdf7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590086"
---
# <a name="connectioncreatequerydef-method-dao"></a>Connection.CreateQueryDef メソッド (DAO)

**適用先**: Access 2013、Office 2013

新しい **[QueryDef](querydef-object-dao.md)** オブジェクトを作成します。

## <a name="syntax"></a>構文

*式* .CreateQueryDef(***Name** _, _*_SQLText_**)

*式***Connection** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>QueryDef</strong> の一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>QueryDef</strong> を定義する SQL ステートメントを表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。この引数を省略した場合、コレクションへの追加前または追加後に、<strong><a href="querydef-sql-property-dao.md">SQL</a></strong> プロパティを設定して、<strong>QueryDef</strong> を定義できます。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

QueryDef

## <a name="remarks"></a>注釈

Microsoft Access ワークスペースでは、**QueryDef** の作成時に名前として長さ 0 の文字列以外を指定すると、作成された **QueryDef** オブジェクトが **[QueryDefs](querydefs-collection-dao.md)** コレクションに自動的に追加されます。

name で指定されたオブジェクトが既に **QueryDefs** コレクションのメンバーである場合は、実行時エラーが発生します。**CreateQueryDef** メソッドの実行時に引数 name に長さ 0 の文字列を指定すると、一時的な **QueryDef** を作成できます。新しく作成した **QueryDef** の **[Name](connection-name-property-dao.md)** プロパティを長さ 0 の文字列 ("") に設定することにより、これを行うこともできます。一時的な **QueryDef** オブジェクトは、**QueryDefs** コレクション内に新しい永続的オブジェクトを作成せずに動的 SQL ステートメントを繰り返し使用する場合に便利です。長さ 0 の文字列は永続的な **QueryDef** オブジェクトの有効な名前ではないので、一時的な **QueryDef** をコレクションに追加することはできません。新しく作成した **QueryDef** オブジェクトの **Name** プロパティと **SQL** プロパティはいつでも設定が可能であり、設定後に **QueryDef** を **QueryDefs** コレクションに追加できます。


            **QueryDef** オブジェクトで SQL ステートメントを実行するには、**[Execute](connection-execute-method-dao.md)** メソッドまたは **[OpenRecordset](connection-openrecordset-method-dao.md)** メソッドを使用します。

ODBC データベースを使用して SQL パススルー クエリを実行する場合は、**QueryDef** オブジェクトの使用をお勧めします。

Microsoft Access データベース エンジンのデータベースで **QueryDefs** コレクションから **QueryDef** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。

