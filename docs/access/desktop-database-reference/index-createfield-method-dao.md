---
title: Index.CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 07835f624c15003d9dfd8fe57bc36a9f598104be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581134"
---
# <a name="indexcreatefield-method-dao"></a>Index.CreateField メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .CreateField(***Name** _, _*_Type_*_, _*_Size_**)

*式* Index オブジェクトを表す **変数** 。

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
<td><p>新しい <strong>Field</strong> オブジェクトの一意の名前を表す文字列型 (String) の値。有効な <strong>Field</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Field

## <a name="remarks"></a>注釈

**CreateField** メソッドを使用して、新しいフィールドを作成し、そのフィールドの名前、データ型、およびサイズを指定できます。**CreateField** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、各プロパティのトピックを参照してください。

type 引数と size 引数は **、TableDef オブジェクト内の Field** オブジェクト **にのみ適用** されます。 **Field** オブジェクトが **Index** または **Relation** オブジェクトに関連付けられている場合、これらの引数は無視されます。

name が既にコレクションのメンバーであるオブジェクトを参照している場合 **[、Append](fields-append-method-dao.md)** メソッドを使用すると実行時エラーが発生します。

**Fields** コレクションから **Field** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスを作成した後は、 **TableDef** オブジェクトの **Fields** コレクションから **Field** オブジェクトを削除できません。

