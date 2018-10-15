---
title: メッセージ テンプレートを使用してメール アイテムを作成する
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 074a3eb7b83e4556b41549d18b81c97b96db1e6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407101"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a>メッセージ テンプレートを使用してメール アイテムを作成する

この例では、[CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)) メソッドを使用してメール アイテムを作成します。

## <a name="example"></a>例

このコード サンプルでは、Ivy.oft テンプレート ファイルを開き、件名を割り当てて、メッセージを下書きフォルダーに保存します。

**CreateItemFromTemplate** メソッドは、ディスクに保存されている Outlook フォーム テンプレート ファイル (.oft) をメッセージ テンプレートとして使用する場合に便利です。メッセージで使用する書式設定済みのテキスト、ひな形、イメージなどを、テンプレート ファイルに格納できます。ただし、テンプレート ファイルにフォームのコードが含まれる場合、フォーム コードは実行されません。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateItemFromTemplate()
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderDrafts), Outlook.Folder)
    Dim mail As Outlook.MailItem = _
        CType(Application.CreateItemFromTemplate( _
        "c:\ivy.oft", folder), Outlook.MailItem)
    mail.Subject = "Congratulations"
    mail.Save()
End Sub
```


```csharp
private void CreateItemFromTemplate()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderDrafts) as Outlook.Folder;
    Outlook.MailItem mail =
        Application.CreateItemFromTemplate(
        @"c:\ivy.oft", folder) as Outlook.MailItem;
    mail.Subject = "Congratulations";
    mail.Save();
}
```

## <a name="see-also"></a>関連項目

- [メール](mail.md)

