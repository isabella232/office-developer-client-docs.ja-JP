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
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a><span data-ttu-id="f0cce-102">プログラムでメッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する</span><span class="sxs-lookup"><span data-stu-id="f0cce-102">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>

<span data-ttu-id="f0cce-103">この例では、電子メール メッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する方法を示します。ディスクに保存された添付ファイルは開くことができます。</span><span class="sxs-lookup"><span data-stu-id="f0cce-103">This example shows how to remove security Level 2 attachments from e-mail messages and save them to a disk, from where they can be opened.</span></span>

## <a name="example"></a><span data-ttu-id="f0cce-104">例</span><span class="sxs-lookup"><span data-stu-id="f0cce-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f0cce-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="f0cce-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f0cce-106">Outlook では、電子メール添付ファイルで送信された特定の拡張子 (.exe や .bat. など) が付いた悪意のあるコードからユーザーが保護されます。</span><span class="sxs-lookup"><span data-stu-id="f0cce-106">Outlook protects users from malicious code transported via e-mail attachments that have certain file extensions such as .exe or .bat.</span></span> <span data-ttu-id="f0cce-107">このような特定の添付ファイルは、既定でブロックされ、レベル 1 の添付ファイルとして識別されます。</span><span class="sxs-lookup"><span data-stu-id="f0cce-107">Those particular attachments are blocked by default and identified as Level 1 attachments.</span></span> <span data-ttu-id="f0cce-108">レベル 2 の添付ファイルの場合、悪意のあるコードが含まれている可能性は低くなりますが、ユーザーが電子メール メッセージからレベル 2 の添付ファイルを直接開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="f0cce-108">Level 2 attachments have a lesser chance of containing malicious code, but users cannot open a Level 2 attachment directly from an e-mail message.</span></span> <span data-ttu-id="f0cce-109">レベル 2 の添付ファイルは、最初にディスクに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0cce-109">A Level 2 attachment must first be saved to a disk.</span></span>

<span data-ttu-id="f0cce-110">[Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) オブジェクトの [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) を使用すると、添付ファイルをディスクに保存できます。</span><span class="sxs-lookup"><span data-stu-id="f0cce-110">By using the [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) method in the [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) object, you can save attachments to a disk.</span></span> <span data-ttu-id="f0cce-111">次のコード例では、RemoveAttachmentsAndSaveToDisk で、まず、フォルダー内にある指定したサイズよりも大きいレベル 2 の添付ファイルをメール アイテムからすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="f0cce-111">In the following code example,   first removes from mail items in a folder all Level 2 attachments that are greater than a specified size.</span></span> <span data-ttu-id="f0cce-112">これは、[Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) コレクション内の各 **Attachment** オブジェクトの [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) プロパティを列挙して、[olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) と等しくなるものを削除することで実行します。</span><span class="sxs-lookup"><span data-stu-id="f0cce-112">This is done by enumerating the [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) property of each **Attachment** object in the [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) collection and removing the ones that are equal to [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) .</span></span> <span data-ttu-id="f0cce-113">その後、RemoveAttachmentsAndSaveToDisk では、削除したファイルを **SaveAsFile** メソッドを使用して保存します。</span><span class="sxs-lookup"><span data-stu-id="f0cce-113"> then saves the removed attachment by using the SaveAsFile method.</span></span>

> [!NOTE] 
> <span data-ttu-id="f0cce-114">Outlook のコレクションは線形です。</span><span class="sxs-lookup"><span data-stu-id="f0cce-114">Collections in Outlook are linear.</span></span> <span data-ttu-id="f0cce-115">**Attachments**[1] から **Attachments**[n] を参照するには、[Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) 演算子を使用します。この n は、[Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia) プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="f0cce-115">Collections in Outlook are linear. Use the P:Microsoft.Office.Interop.Outlook.Attachment.Index[n] operator to reference Attachments[1] to Attachments[n] where n represents the value of the P:Microsoft.Office.Interop.Outlook.Attachments.Count property.</span></span>
> 
> <span data-ttu-id="f0cce-p104">**foreach** ステートメントを使用してコレクション内のアイテムを削除することはできません。代わりに、**Index** 演算子を使用してコレクションの最初のアイテムを取得し、そのアイテムを削除します。次に、**while** ステートメントを使用して、コレクションから適切な数のアイテムを削除したことを判別します。これにより、コレクション内の正しい数のアイテムを確実に反復処理できます。</span><span class="sxs-lookup"><span data-stu-id="f0cce-p104">You cannot use a **foreach** statement to remove items in a collection. Instead, use an **Index** operator to obtain the first item in the collection, and then delete the item. Then use a **while** statement to determine when you have deleted the appropriate number of items in the collection. This will ensure that you have iterated over the correct number of items in the collection.</span></span>

<span data-ttu-id="f0cce-120">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0cce-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f0cce-121">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0cce-121">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f0cce-122">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f0cce-122">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f0cce-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0cce-123">See also</span></span>

- [<span data-ttu-id="f0cce-124">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="f0cce-124">Attachments</span></span>](attachments.md)
