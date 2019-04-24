---
title: CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae322277dd1d357aceb3f9129110dded705f9eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307064"
---
# <a name="relationcreatefield-method-dao"></a>CreateField メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。CreateField (***名前***、***種類***、***サイズ***)

*式***Relation**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Field</strong> オブジェクトの一意の名前を表す文字列型 (String) の値。 有効な<strong>フィールド</strong>名の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong>プロパティを参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Field

## <a name="remarks"></a>注釈

**CreateField** メソッドを使用して、新しいフィールドを作成し、そのフィールドの名前、データ型、およびサイズを指定できます。**CreateField** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、各プロパティのトピックを参照してください。

引数 type および引数 size は、 **TableDef**オブジェクトの**Field**オブジェクトにのみ適用されます。 これらの引数は、 **Field** オブジェクトが **Index** オブジェクトまたは **Relation** オブジェクトに関連付けられている場合は無視されます。

name が既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。

**Fields** コレクションから **Field** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスを作成した後は、 **TableDef** オブジェクトの **Fields** コレクションから **Field** オブジェクトを削除できません。

