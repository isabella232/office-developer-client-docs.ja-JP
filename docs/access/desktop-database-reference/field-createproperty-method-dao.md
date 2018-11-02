---
title: Field.CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: b3c1d303-7cab-89c3-8e90-f18a0445d304
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822050(v=office.15)
ms:contentKeyID: 48547202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71d5a77543de05cd440e5b5c2cf40596d141b16d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926151"
---
# <a name="fieldcreateproperty-method-dao"></a>Field.CreateProperty メソッド (DAO)


**適用されます**Access 2013、Office 2013。

新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。CreateProperty (***名前***、***型***、***値***、 ***DDL***)

*式***Field**オブジェクトを表す変数です。

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
<td><p>新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="even">
<td><p>型</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="odd">
<td><p>値</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="even">
<td><p>DDL</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p><strong>バリアント型</strong>(<strong>ブール型</strong>のサブタイプ)<strong>プロパティ</strong>は、DDL オブジェクトであるかどうかを示す。 既定では <strong>False です</strong> 。 DDL が<strong>True</strong>の場合は、ユーザーが変更または<strong>dbSecWriteDef</strong>権限を持たない<strong>プロパティ</strong>オブジェクトを削除できません。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>戻り値

プロパティ

## <a name="remarks"></a>注釈

ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。

**CreateProperty** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。

名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。

ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 [Properties](fields-delete-method-dao.md) コレクションの ****Delete**** メソッドを使用します。組み込みのプロパティは削除できません。


> [!NOTE]
> DDL 引数を省略した場合のデフォルト値は False (DDL 以外)。 対応する DDL プロパティは公開されていないので、DDL から DDL 以外に変更する **Property** オブジェクトを削除し、再作成する必要があります。


