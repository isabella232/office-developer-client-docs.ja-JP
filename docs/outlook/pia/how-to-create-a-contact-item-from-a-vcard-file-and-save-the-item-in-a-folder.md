---
title: vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a048d090c946ff5a86fddf4b1ac8c6818e061b1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698849"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a><span data-ttu-id="f8e88-102">vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する</span><span class="sxs-lookup"><span data-stu-id="f8e88-102">Create a Contact item from a vCard file and save the item in a folder</span></span>

<span data-ttu-id="f8e88-103">この例では、ファイル システムのフォルダーに入っているすべての vCard ファイルをインポートし、連絡先を *targetFolder* パラメーターで指定されたフォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="f8e88-103">This example imports all the vCard files in a file system folder and saves the contacts into the folder specified by the *targetFolder* parameter.</span></span>

## <a name="example"></a><span data-ttu-id="f8e88-104">例</span><span class="sxs-lookup"><span data-stu-id="f8e88-104">Example</span></span>

<span data-ttu-id="f8e88-p101">次の例では、 [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) メソッドを使用します。 **OpenSharedItem** メソッドは、Outlook メッセージ形式 (.msg) ファイル、iCalendar 予定 (.ics) ファイル、または vCard (.vcf) ファイルとして格納されているメッセージを開きます。アイテムを保存するには、返されたオブジェクトを適切なアイテムの種類にキャストし、対応する **Save** メソッドを呼び出します。既定では、 **OpenSharedItem** によって返されるアイテムは、特定のアイテムの種類に対する既定のフォルダーに保存されます。対応する **Move** メソッドを使用すると、アイテムを別のフォルダーに移動できます。</span><span class="sxs-lookup"><span data-stu-id="f8e88-p101">This example uses the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method. The **OpenSharedItem** method opens messages stored as Outlook message format (.msg) files, iCalendar appointment (.ics) files, or vCard (.vcf) files. Be sure to cast the returned object to the appropriate item type and call the corresponding **Save** method to persist the item. By default, the item returned by **OpenSharedItem** is saved in the default folder for the specific item type. You can use the corresponding **Move** method to move the item to a different folder.</span></span>

<span data-ttu-id="f8e88-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8e88-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f8e88-111">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8e88-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f8e88-112">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f8e88-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f8e88-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8e88-113">See also</span></span>

- [<span data-ttu-id="f8e88-114">連絡先</span><span class="sxs-lookup"><span data-stu-id="f8e88-114">Contacts</span></span>](contacts.md)

