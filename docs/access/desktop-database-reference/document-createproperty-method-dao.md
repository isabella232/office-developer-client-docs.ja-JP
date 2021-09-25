---
title: Document.CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 1ed56d43d68de1da03a2bcf47396547951c1b4b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569063"
---
# <a name="documentcreateproperty-method-dao"></a>Document.CreateProperty メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .CreateProperty(***Name** _, _*_Type_*_, _*_Value_*_, _*_DDL_**)

*式* Document オブジェクトを表す **変数** 。

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
<td><p>新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>オプション</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>オプション</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Property</strong> が DDL オブジェクトであるかどうかを示す、サブタイプがブール型 (<strong>Boolean</strong>) であるバリアント型 (<strong>Variant</strong>) の値。既定値は <strong>False</strong> です。DDL が <strong>True</strong> の場合、ユーザーは <strong>dbSecWriteDef</strong> 権限を持っていない限り、この <strong>Property</strong> オブジェクトを変更または削除することができません。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

プロパティ

## <a name="remarks"></a>注釈

ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。

**CreateProperty** を使用するときに 1 つ以上の省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトをコレクションに追加した後は、一部のプロパティ設定を変更できなくなります。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。

name が既にコレクションのメンバーであるオブジェクトを参照している場合 **[、Append](fields-append-method-dao.md)** メソッドを使用すると実行時エラーが発生します。

ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 **[Properties](fields-delete-method-dao.md)** コレクションの **Delete** メソッドを使用します。組み込みのプロパティは削除できません。


> [!NOTE]
> DDL 引数を省略すると、既定値は False (非 DDL) になります。 対応する DDL プロパティは公開されないため、 **Property** オブジェクトを DDL から非 DDL に変更する場合は、そのオブジェクトを削除して再作成する必要があります。


