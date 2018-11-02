---
title: QueryDefs.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d757bf9d05c829e41af97cac6a30ffb064a3b113
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929728"
---
# <a name="querydefsappend-method-dao"></a>QueryDefs.Append メソッド (DAO)


**適用されます**Access 2013、Office 2013。

新しい **QueryDef** を **QueryDefs** コレクションに追加します。

## <a name="syntax"></a>構文

*式*です。(***オブジェクト***) を追加します。

*式***クエリ定義**オブジェクトを表す変数です。

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
<td><p>オブジェクト</p></td>
<td><p>必須</p></td>
<td><p><strong>オブジェクト型 (Object)</strong></p></td>
<td><p>コレクションに追加するフィールドを表すオブジェクト変数です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。

新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。

追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。 たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。

