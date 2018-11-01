---
title: '手順 3: Fields リスト ボックスに値を設定する'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae1513c47c79da4f4df7fee2f3f3d7b3507ac1c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876660"
---
# <a name="step-3-populate-the-fields-list-box"></a>手順 3: Fields リスト ボックスに値を設定する


**適用されます**Access 2013、Office 2013。

## <a name="step-3-populate-the-fields-list-box"></a>手順 3: Fields リスト ボックスの設定

**Fields リスト ボックスに値を設定するには**

lstMain の Click イベント ハンドラーに次のコードを挿入します。

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

このコードを宣言し、ローカル**レコード**と**レコード セット**オブジェクト、レコードのインスタンスを作成し、rs、それぞれ。

LstMain 内で選択されたリソースに対応する行には、grs の現在の行が行われます。 **[詳細**] ボックスの一覧ボックスがオフになってとの現在の行にレコードを開きます。 **詳細**のリスト ボックスをオフにし、およびソースとして grs の現在の行にレコードを開きます。

リソースがコレクション レコード ( **RecordType**で指定) と同じである場合は、レコードの子で、ローカル**レコード セット**rs が開かれます。LstDetails の行から値を入力し、レコードの子で開かれます。[LstDetails rs の行から値が入力されます。

リソースが単純レコードである場合は、recFields が呼び出されます。recFields の詳細については、次の手順を参照してください。

リソースが構造化ドキュメントである場合は、コードは実装されません。

