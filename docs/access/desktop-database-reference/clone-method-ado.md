---
title: Clone メソッド - ActiveX データ オブジェクト (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ec081c42a219e7073041998826b533a1b0fa6c81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627080"
---
# <a name="clone-method-ado"></a>Clone メソッド (ADO)

**適用先**: Access 2013、Office 2013

既存の [Recordset](recordset-object-ado.md) オブジェクトから **Recordset** オブジェクトの複製を作成します。必要に応じて、複製を読み取り専用に指定できます。

## <a name="syntax"></a>構文

 *rstDuplicate*  =  *rstOriginal を設定します*。Clone (*LockType*)

## <a name="return-value"></a>戻り値

**Recordset** オブジェクトの参照を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*rstDuplicate* |作成する **Recordset** オブジェクトの複製を示すオブジェクト変数です。|
|*rstOriginal* |複製元の **Recordset** オブジェクトを示すオブジェクト変数です。|
|*LockType* |省略可能です。複製元 [Recordset](locktypeenum.md) のロックの種類にするか、または読み取り専用 **Recordset** にするかを指定する、 **LockTypeEnum** の値です。有効な値は、 **adLockUnspecified** または **adLockReadOnly** です。|

## <a name="remarks"></a>注釈

**Clone** メソッドは、**Recordset** オブジェクトの複製を複数作成する場合に使用します。特に、レコードセットの複数のカレント レコードを保持したい場合には、このメソッドを使用します。**Clone** メソッドを使用した方が、元の **Recordset** オブジェクトと同じ定義で新しいオブジェクトを作成して開くよりも効率的です。

元の [Recordset](filter-property-ado.md) で **Filter** プロパティが設定されていても、複製には適用されません。結果をフィルターするには、新しい **Recordset** の **Filter** プロパティを設定する必要があります。既存の **Filter** 値をコピーする最も簡単な方法は、

のように値を直接代入することです。

1 つの **Recordset** オブジェクトに加えた変更は、カーソルの種類に関係なく、すべての複製で表示できます。ただし、複製元の [Recordset](requery-method-ado.md) で **Requery** を実行した後は、複製は複製元の Recordset とは同期しなくなります。

複製元の **Recordset** を閉じても、その複製は開いたままです。また、1 つの複製を閉じても、複製元または他の複製は開いたままになります。

複製できるのは、ブックマークをサポートする **Recordset** オブジェクトだけです。ブックマークの値は交換可能です。つまり、1 つの **Recordset** オブジェクトのブックマーク参照は、すべての複製の同じレコードを参照します。

発生する **Recordset** イベントの中には、すべての **Recordset** 複製において発生するものがあります。ただし、複製された **Recordset** によってカレント レコードが異なる可能性があるため、複製ではイベントが無効である場合もあります。

たとえば、あるフィールドの値を変更すると、変更された **Recordset** とすべての複製で、[WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) イベントが発生します。複製された (変更されていない) **Recordset** の **WillChangeField** イベントの *Fields* パラメーターは、その複製のカレント レコードのフィールドを参照するだけであり、変更が発生した元の **Recordset** のカレント レコードとは異なる可能性があります。

次の表は、すべての **Recordset** イベントの一覧と、**Clone** メソッドを使用して生成されたすべてのレコードセット複製に対してそのイベントが有効で発生するかどうかを示しています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>イベント</p></th>
<th><p>複製で発生するか</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>いいえ</p></td>
</tr>
</tbody>
</table>

