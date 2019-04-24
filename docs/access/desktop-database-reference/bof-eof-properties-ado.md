---
title: BOF プロパティと EOF プロパティ (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296788"
---
# <a name="bof-eof-properties-ado"></a>BOF プロパティと EOF プロパティ (ADO)


**適用先:** Access 2013、Office 2013

**BOF** カレント レコードの位置が [Recordset](recordset-object-ado.md) オブジェクトの最初のレコードより前にあることを示します。

**EOF** カレント レコードの位置が **Recordset** オブジェクトの最後のレコードより後にあることを示します。

## <a name="return-value"></a>戻り値

**BOF** プロパティと **EOF** プロパティは、ブール型 (**Boolean**) の値を返します。

## <a name="remarks"></a>注釈

**BOF** プロパティと **EOF** プロパティを使用すると、**Recordset** オブジェクトにレコードが格納されているかどうかを調べたり、レコード間を移動したときに **Recordset** オブジェクトの範囲を越えていないかを調べたりすることができます。

**BOF** プロパティは、カレント レコードの位置が先頭レコードより前にある場合に **True** (-1) を返し、カレント レコードの位置が先頭レコードにあるか、またはそれより後ろにある場合に **False** (0) を返します。

**EOF** プロパティは、カレント レコードの位置が最後のレコードより後ろにある場合に **True** を返し、カレント レコードの位置が最後のレコードにあるか、またはそれより前にある場合に **False** を返します。

**BOF** プロパティと **EOF** プロパティのいずれかが **True** になっている場合は、カレント レコードが存在しません。

レコードが 1 つも格納されていない **Recordset** オブジェクトを開くと、**BOF** プロパティと **EOF** プロパティが **True** に設定されます (**Recordset** のこの状態については、[RecordCount](recordcount-property-ado.md) プロパティの説明を参照してください)。1 つ以上のレコードが格納されている **Recordset** オブジェクトを開くと、先頭レコードがカレント レコードになり、**BOF** プロパティと **EOF** プロパティが **False** に設定されます。

**Recordset** オブジェクトに残っている最後の 1 つのレコードを削除した場合は、カレント レコードの位置を変更しようとするまでは **BOF** プロパティと **EOF** プロパティが **False** のまま変わらないこともあります。

次の表に、 **BOF** プロパティと **EOF** プロパティのさまざまな組み合わせで、どの **Move** メソッドが使用できるかを示します。

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst<br />
MoveLast</p></th>
<th><p>MovePrevious<br />
移動&lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext<br />
移動&gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = True、</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>可</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>可</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False、</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
</tr>
<tr class="odd">
<td><p>両方とも <strong>True</strong></p></td>
<td><p>エラー</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>エラー</p></td>
</tr>
<tr class="even">
<td><p>両方とも <strong>False</strong></p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>可</p></td>
</tr>
</tbody>
</table>


**Move** メソッドが使用可となっている場合、そのメソッドがレコードを正常に配置できるという保証をしているわけではありません。その **Move** メソッドを呼び出してもエラーが発生しないことを意味しているだけです。

次の表は、各種 **Move** メソッドを呼び出して、正常にレコードを配置できなかった場合に、**BOF** プロパティと **EOF** プロパティの設定がどうなるかを示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>、 <strong>MoveLast</strong></p></td>
<td><p><strong>True</strong> に設定</p></td>
<td><p><strong>True</strong> に設定</p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>変化なし</p></td>
<td><p>変化なし</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</p></td>
<td><p><strong>True</strong> に設定</p></td>
<td><p>変化なし</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>、 <strong>Move</strong> &gt; 0</p></td>
<td><p>変化なし</p></td>
<td><p><strong>True</strong> に設定</p></td>
</tr>
</tbody>
</table>

