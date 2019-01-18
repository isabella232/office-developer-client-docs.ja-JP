---
title: Recordset.EOF プロパティ (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 931de7dfc2cfb80726aafe7077c6107ec65d2f40
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719492"
---
# <a name="recordseteof-property-dao"></a>Recordset.EOF プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

カレント レコードの位置が、 **Recordset** オブジェクトの最後のレコードより後にあるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。EOF

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**BOF** プロパティおよび **EOF** プロパティを使用すると、 **Recordset** オブジェクトにレコードが格納されているかどうかの確認、またはレコード間を移動したときに **Recordset** オブジェクトの範囲を超えたかどうかの確認ができます。

カレント レコードを参照するポインターの位置により、 **BOF** および **EOF** の戻り値が決まります。

**BOF** プロパティまたは **EOF** プロパティのどちらかが **True** の場合は、カレント レコードが存在しません。

レコードを含まない **Recordset** オブジェクトを開くと、 **BOF** プロパティおよび **EOF** プロパティが **True** に設定され、 **Recordset** オブジェクトの **RecordCount** プロパティの設定値が 0 になります。少なくとも 1 つのレコードを含む **Recordset** オブジェクトを開くと、最初のレコードがカレント レコードになり、 **BOF** プロパティおよび **EOF** プロパティが **False** になって、 **MovePrevious** メソッドまたは **MoveNext** メソッドを使用して **Recordset** オブジェクトの先頭または末尾を越えて移動するまで **False** のままになります。 **Recordset** オブジェクトの先頭または末尾を越えて移動すると、カレント レコードがないか、またはレコードが存在しなくなります。

**Recordset** オブジェクト内に残っている最後のレコードを削除すると、カレント レコードを再配置しようとするまで **BOF** プロパティおよび **EOF** プロパティは **False** のままになります。

レコードを含む **Recordset** オブジェクトで **MoveLast** メソッドを使用すると、最後のレコードがカレント レコードになり、その後 **MoveNext** メソッドを使用すると、カレント レコードが無効になり、 **EOF** プロパティが **True** に設定されます。一方、レコードを含む **Recordset** オブジェクトで **MoveFirst** メソッドを使用すると、最初のレコードがカレント レコードになり、その後 **MovePrevious** メソッドを使用すると、カレント レコードがなく、 **BOF** プロパティが **True** に設定されます。

通常、 **Recordset** オブジェクトのすべてのレコードを操作する場合は、 **EOF** プロパティが **True** に設定されるまで **MoveNext** メソッドを使用してレコード内をループするコードを記述します。

**EOF** プロパティが **True** に設定されている場合に **MoveNext** メソッドを使用するか、または **BOF** プロパティが **True** に設定されている場合に **MovePrevious** メソッドを使用すると、エラーが発生します。

次の表は、 **BOF** プロパティおよび **EOF** プロパティのさまざまな組み合わせで使用できる Move メソッドの種類を示しています。

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
<th><p>MoveFirst、<br />
MoveLast</p></th>
<th><p>MovePrevious、<br />
移動&lt;0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext、<br />
移動&gt;0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = true の場合、</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>可</p></td>
<td><p>エラー</p></td>
<td><p>エラー</p></td>
<td><p>可</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False の場合、</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>エラー</p></td>
<td><p>エラー</p></td>
</tr>
<tr class="odd">
<td><p>両方とも <strong>True</strong></p></td>
<td><p>エラー</p></td>
<td><p>エラー</p></td>
<td><p>エラー</p></td>
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


Move メソッドが使用可となっていても、そのメソッドがレコードを正常に配置できるとは限りません。指定された Move メソッドを実行しようとすることが許可されていて、エラーが発生しないことを意味しているだけです。 **BOF** プロパティおよび **EOF** プロパティの状態は、試みた Move メソッドの結果によって変わる可能性があります。

**OpenRecordset** メソッドは、 **MoveFirst** メソッドを内部的に呼び出します。したがって、空のレコードのセットに対して **OpenRecordset** メソッドを使用すると、 **BOF** プロパティおよび **EOF** プロパティが **True** に設定されます (失敗した **MoveFirst** メソッドの動作については、次の表を参照)。

Move メソッドを使用してレコードが正常に配置される場合は常に、 **BOF** プロパティと **EOF** の両方が **False** に設定されます。

Microsoft Access ワークスペースでは、レコードを空の **Recordset** オブジェクトに追加すると、 **BOF** プロパティが **False** になりますが、 **EOF** プロパティは **True** のままで、現在の位置が **Recordset** の末尾であることを示します。

いずれかの **Delete** メソッドを使用して、 **Recordset** に 1 つのみ残っているレコードを削除しても、 **BOF** プロパティおよび **EOF** プロパティの設定は変更されません。

次の表は、Move メソッドでレコードが配置されなかった場合に、 **BOF** プロパティおよび **EOF** プロパティがどのように設定されるかを示しています。

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
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>変化なし</p></td>
<td><p>変化なし</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>変化なし</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>、<strong>移動</strong> &gt; 0</p></td>
<td><p>変化なし</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

