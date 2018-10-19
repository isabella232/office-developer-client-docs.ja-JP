---
title: 既定のフォルダーを取得して、そのサブフォルダーを列挙する
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 934b5f823127fde9fbbd3a49f41cedb791277e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407402"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a><span data-ttu-id="449db-102">既定のフォルダーを取得して、そのサブフォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="449db-102">Get a default folder and enumerate its subfolders</span></span>

<span data-ttu-id="449db-103">この例では、ユーザーの既定のストア内の既定のフォルダーを取得して、そのサブフォルダーを列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="449db-103">This example shows how to obtain a default folder in the user’s default store and enumerate its subfolders.</span></span>

## <a name="example"></a><span data-ttu-id="449db-104">例</span><span class="sxs-lookup"><span data-stu-id="449db-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="449db-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="449db-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="449db-106">次のコード例では、GetRSSFeeds が [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) メソッドを使用して、ユーザーの RSS Feeds ルート フォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="449db-106">In the following code example,   uses the GetDefaultFolder(OlDefaultFolders) method of the NameSpace object to obtain the user's RSS Feeds root folder.</span></span> <span data-ttu-id="449db-107">次に、GetRSSFeeds は RSS Feeds フォルダー内のすべての RSS フィードに対するフォルダーの名前を含むメッセージ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="449db-107"> then displays a message box that contains the folder names for all RSS feeds in the RSS Feeds folder.</span></span>

<span data-ttu-id="449db-108">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="449db-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="449db-109">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="449db-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="449db-110">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="449db-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetRSSFeeds()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderRssFeeds)
        as Outlook.Folder;
    if (folder != null)
    {
        if (folder.Folders.Count > 0)
        {
            StringBuilder sb = new StringBuilder();
            foreach (Outlook.Folder subfolder
                in folder.Folders)
            {
                sb.AppendLine(subfolder.Name);
            }
            MessageBox.Show(sb.ToString(),
                "RSS Feeds",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="449db-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="449db-111">See also</span></span>

- [<span data-ttu-id="449db-112">フォルダー</span><span class="sxs-lookup"><span data-stu-id="449db-112">Folders</span></span>](folders.md)

