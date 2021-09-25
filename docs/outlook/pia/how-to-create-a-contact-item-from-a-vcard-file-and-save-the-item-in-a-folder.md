---
title: vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7ced53d60b67d75caedccbb87b83947861d25f9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623797"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a>vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する

この例では、ファイル システムのフォルダーに入っているすべての vCard ファイルをインポートし、連絡先を *targetFolder* パラメーターで指定されたフォルダーに保存します。

## <a name="example"></a>例

次の例では、 [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) メソッドを使用します。 **OpenSharedItem** メソッドは、Outlook メッセージ形式 (.msg) ファイル、iCalendar 予定 (.ics) ファイル、または vCard (.vcf) ファイルとして格納されているメッセージを開きます。アイテムを保存するには、返されたオブジェクトを適切なアイテムの種類にキャストし、対応する **Save** メソッドを呼び出します。既定では、 **OpenSharedItem** によって返されるアイテムは、特定のアイテムの種類に対する既定のフォルダーに保存されます。対応する **Move** メソッドを使用すると、アイテムを別のフォルダーに移動できます。

Visual Studio を使用してこのコード サンプルをテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートする際に、最初に必ず Microsoft Outlook 15.0 Object Library コンポーネントへの参照を追加し、そして Outlook 変数を指定します。**Imports** または **using** ステートメントは、コード サンプル中の関数の前に直接置かれず、Public クラス宣言の前に追加する必要があります。次のプログラムは、Visual Basic および C\#でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [連絡先](contacts.md)

