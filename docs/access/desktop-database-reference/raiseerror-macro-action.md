---
title: RaiseError マクロ アクション
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300925"
---
# <a name="raiseerror-macro-action"></a>RaiseError マクロ アクション

**適用先:** Access 2013、Office 2013 

The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.

> [!NOTE]
> The **RaiseError** action is available only in Data Macros.

## <a name="setting"></a>Setting

"RaiseError/エラーの生成" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>エラー番号</p></td>
<td><p>はい</p></td>
<td><p>長整数型のデータ入力に解決される数値または式。</p></td>
</tr>
<tr class="even">
<td><p>Error Description/エラー説明</p></td>
<td><p>いいえ</p></td>
<td><p>エラーを説明する文字列式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.

If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.

To see the **USysApplicationLog** table, use the following steps:

1.  [**ファイル**] メニューをクリックし、[**オプション**] をクリックします。

2.  [ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。

3.  [ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。

4.  [ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。

5.  [ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。

## <a name="example"></a>例

次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。 AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。 これが true の場合、Before Change イベントは取り消され、レコードは更新されません。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
