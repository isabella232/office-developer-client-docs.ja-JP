---
title: プログラムでメッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 3646ff17a6200a6b46b7796537a40e7bdab40781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406597"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a>プログラムでメッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する

この例では、電子メール メッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する方法を示します。ディスクに保存された添付ファイルは開くことができます。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Outlook では、電子メール添付ファイルで送信された特定の拡張子 (.exe や .bat. など) が付いた悪意のあるコードからユーザーが保護されます。 このような特定の添付ファイルは、既定でブロックされ、レベル 1 の添付ファイルとして識別されます。 レベル 2 の添付ファイルの場合、悪意のあるコードが含まれている可能性は低くなりますが、ユーザーが電子メール メッセージからレベル 2 の添付ファイルを直接開くことはできません。 レベル 2 の添付ファイルは、最初にディスクに保存する必要があります。

[Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) オブジェクトの [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) を使用すると、添付ファイルをディスクに保存できます。 次のコード例では、RemoveAttachmentsAndSaveToDisk で、まず、フォルダー内にある指定したサイズよりも大きいレベル 2 の添付ファイルをメール アイテムからすべて削除します。 これは、[Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) コレクション内の各 **Attachment** オブジェクトの [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) プロパティを列挙して、[olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) と等しくなるものを削除することで実行します。 その後、RemoveAttachmentsAndSaveToDisk では、削除したファイルを **SaveAsFile** メソッドを使用して保存します。

> [!NOTE] 
> Outlook のコレクションは線形です。 **Attachments**[1] から **Attachments**[n] を参照するには、[Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) 演算子を使用します。この n は、[Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia) プロパティの値を表します。
> 
> **foreach** ステートメントを使用してコレクション内のアイテムを削除することはできません。代わりに、**Index** 演算子を使用してコレクションの最初のアイテムを取得し、そのアイテムを削除します。次に、**while** ステートメントを使用して、コレクションから適切な数のアイテムを削除したことを判別します。これにより、コレクション内の正しい数のアイテムを確実に反復処理できます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RemoveAttachmentsAndSaveToDisk(string path,
    Outlook.Folder folder, int size)
{
    Outlook.Items attachItems;
    Outlook.Attachment attachment;
    Outlook.Attachments attachments;
    int byValueCount;
    int removeCount;
    bool saveMessage;
    try
    {
        // The restriction will find all items that
        // have attachments and MessageClass = IPM.Note.
        string filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:hasattachment"
            + "\"" + " = True" + " AND " + "\""
            + "https://schemas.microsoft.com/mapi/proptag/0x001A001E"
            + "\"" + " = 'IPM.Note'";
        attachItems = folder.Items.Restrict(filter);
        foreach (Outlook.MailItem mail in attachItems)
        {
            saveMessage = false;
            byValueCount = 0;
            attachments = mail.Attachments;
            // Obtain the count of ByValue attachments.
            foreach (Outlook.Attachment attach in attachments)
            {
                if (attach.Size > size
                    & attach.Type ==
                    Outlook.OlAttachmentType.olByValue)
                {
                    byValueCount = byValueCount + 1;
                }
            }
            if (byValueCount > 0)
            {
                // removeCount is number of attachments to remove.
                removeCount = attachments.Count - byValueCount;
                while (mail.Attachments.Count != removeCount)
                {
                    // Use indexer to obtain 
                    // first attachment in collection.
                    attachment = mail.Attachments[1];
                    // You can refine this code to save 
                    // separate copies of attachments 
                    // with the same name.
                    attachment.SaveAsFile(path + @"\"
                        + attachment.FileName);
                    attachment.Delete();
                    if (saveMessage != true)
                    {
                        saveMessage = true;
                    }
                }
                if (saveMessage)
                {
                    mail.Save();
                }
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>関連項目

- [添付ファイル](attachments.md)

