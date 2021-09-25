---
title: フォルダーを列挙する
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50af2d229847121ca5395b69c33c533ff5d2f651
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560573"
---
# <a name="enumerate-folders"></a>フォルダーを列挙する

この例では、フォルダーのコレクションを反復処理することでフォルダーを列挙する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード例では、まず EnumerateFoldersInDefaultStore メソッドが [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) メソッドを使用して、既定のストアのルート フォルダーを取得します。 次に、ルート フォルダーで EnumerateFolders メソッドを呼び出します。 EnumerateFolders はルート フォルダーを取得し、ルート フォルダーが表している既定のストアのフォルダーをウォークスルーします。 EnumerateFolders は、まず [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) プロパティを使用してルートの [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトのサブフォルダーを取得します。 次に、階層内のすべてのフォルダーを列挙するために、EnumerateFolders が繰り返し呼び出されます。 最後に、EnumerateFolders は各 **Folder** の [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) プロパティを [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクション内のトレース リスナーに書き込みます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>関連項目

- [フォルダー](folders.md)

