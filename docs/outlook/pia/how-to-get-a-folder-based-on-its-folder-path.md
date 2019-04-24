---
title: フォルダーのパスに基づいてフォルダーを取得する
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fed1e7eb39f31ddd4340fc82a16e31ec67523a9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320287"
---
# <a name="get-a-folder-based-on-its-folder-path"></a>フォルダーのパスに基づいてフォルダーを取得する

この例では、フォルダー パスを取得して関連するフォルダーを取得します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

このコード例の GetKeyContacts メソッドは、[GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) プロパティを使用して Contacts\\Key Contacts フォルダーのフォルダー パスを取得します。 次に、[FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) プロパティを引数として使用して、GetFolder メソッドを呼び出します。 GetFolder がフォルダーを返すと、Key Contacts が見つかったことを示すメッセージが表示されます。 GetFolder メソッドはフォルダーへのパスを取得して、適切な [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトを返します。 この処理は、まず **FolderPath** プロパティを string 配列に分割し、次にその配列を使用して **FolderPath** プロパティの先頭から始まる適切な **Folder** オブジェクトを検出することによって実行されます。 指定されたフォルダーが見つからない場合、GetFolder は NULL 参照を返します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a>関連項目

- [フォルダー](folders.md)

