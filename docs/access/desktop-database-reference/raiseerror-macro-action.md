---
title: "'RaiseError/エラーの生成' マクロ アクション"
TOCTitle: RaiseError Macro Action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 134222e825826615feb495adaae6296229edb868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476715"
---
# <a name="raiseerror-macro-action"></a>"RaiseError/エラーの生成" マクロ アクション

**適用されます**Access 2013 |。Office 2013 

**RaiseError**アクションは、**[エラー時](onerror-macro-action.md)** のマクロ アクションで処理できる例外をスローします。

> [!NOTE]
> [!メモ] " **RaiseError** /エラーの生成" アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

**RaiseError**アクションには、次の引数があります。

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
<td><p>Error Number/エラー番号</p></td>
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


## <a name="remarks"></a>備考

**RaiseError**アクションは、**[前に変更](before-change-macro-event.md)** または**[削除をする前に](before-delete-macro-event.md)** マクロのイベントで呼び出されると、イベントはキャンセルされます。

エラーの処理は、**エラー時**のアクティブなステートメントがない場合、 **RaiseError**操作によってスローされたエラーは、 **USysApplicationLog**システム ・ テーブルに追加されます。 **RaiseError**の動作は、 **USysApplicationLog**テーブルに書き込み、 **[カテゴリ**] 列が自動的に**実行**する設定します。

**USysApplicationLog**テーブルを表示するには、次の手順に従います。

1.  [**ファイル**] メニューのをクリックし、[**オプション**] をクリックします。

2.  [ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。

3.  [ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。

4.  [ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。

5.  [ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。

## <a name="example"></a>例

次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。 AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。 これが true の場合は、変更する前にイベントをキャンセルするとレコードは更新されません。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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
