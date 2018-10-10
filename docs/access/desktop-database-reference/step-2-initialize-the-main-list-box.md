---
title: '手順 2: Main リスト ボックスを初期化する'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478632"
---
# <a name="step-2-initialize-the-main-list-box"></a>手順 2: Main リスト ボックスを初期化する


**適用されます**Access 2013 |。Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>手順 2: Main リスト ボックスを初期化する

**グローバルな Record オブジェクトと Recordset オブジェクトを宣言するには**

  - Form1 の (General) (Declarations) に次のコードを挿入します。
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。

**URL に接続して lstMain にデータを設定するには**

  - Form1 の Form Load イベント ハンドラーに次のコードを挿入します。
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。 **レコード**grec、 **ActiveConnection**として指定された URL を使用して開かれます。 URL が存在する場合は開かれますが、存在しない場合は作成されます。 "https://servername/foldername/" は、使用する環境での有効な URL に置き換える必要があります。 **レコード**grec の子の**レコード セット**grs が開かれます。 次に、URL に発行されたリソースのファイル名が lstMain に設定されます。

