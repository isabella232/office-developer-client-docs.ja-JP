---
title: Relation.CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 564cbae4669a0405a0e33d0e9770bbaa8f6c9dfb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929483"
---
# <a name="relationcreatefield-method-dao"></a>Relation.CreateField メソッド (DAO)


**適用されます**Access 2013、Office 2013。

新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。CreateField (***名前***、***種類***、***サイズ***)

*式***Relation**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<td><p>名前</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>新しい <strong>Field</strong> オブジェクトの一意の名前を表す文字列型 (String) の値。有効な <strong>Field</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</p></td>
</tr>
<tr class="even">
<td><p>型</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
<tr class="odd">
<td><p>サイズ</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>戻り値

Field

## <a name="remarks"></a>注釈

**CreateField** メソッドを使用すると、新しいフィールドを作成して、そのフィールドの名前、データ型、およびサイズを指定できます。 **CreateField** を使用するときに 1 つ以上のオプションの引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトをコレクションに追加した後は、一部のプロパティ設定を変更できなくなります。詳細については、各プロパティのトピックを参照してください。

タイプとサイズの引数は、**テーブル定義**オブジェクト内の**Field**オブジェクトのみに適用されます。 これらの引数は、 **Field** オブジェクトが **Index** オブジェクトまたは **Relation** オブジェクトに関連付けられている場合は無視されます。

名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。

**Field** オブジェクトを **Fields** コレクションから削除するには、そのコレクションで **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスの作成後は、その **Field** オブジェクトを **TableDef** オブジェクトの **Fields** コレクションから削除できません。

