---
title: フォルダーのアカウントを取得する
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8f56f866e71b1080d5b7a6a33fb17e3e71ab9199
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708096"
---
# <a name="get-the-account-for-a-folder"></a>フォルダーのアカウントを取得する

この例では、現在のセッションで特定のフォルダーに関連付けられているアカウントを取得します。

## <a name="example"></a>例

以下のコード例の DisplayAccountForCurrentFolder 関数は GetAccountForFolder 関数を呼び出して、現在のフォルダーをホストしている既定の配信ストアのアカウントを特定し、そのフォルダーの名前を表示します。 GetAccountForFolder は、現在のフォルダーのストア ([Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) プロパティから取得) を、セッションの [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) コレクションで定義されている各アカウントの既定の配信ストア ([DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) プロパティで取得) と照合します。 GetAccountForFolder は、一致するものが見つかった場合は [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを返し、見つからなかった場合は Null 参照を返します。

Microsoft Outlook セッションでプロファイルに複数のアカウントが定義されているとき、アクティブなエクスプローラーに表示されるフォルダーは、そのセッションの既定のストアには必ずしも存在せず、複数のアカウントに関連付けられた複数のストアのいずれかに存在します。このトピックでは、既定の配信ストアがフォルダーをホストしているストアでもあるときに、そのアカウントを特定する方法を示しています。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayAccountForCurrentFolder()
{
    Outlook.Folder myFolder = Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    string msg = "Account for Current Folder:" + "\n" +
        GetAccountForFolder(myFolder).DisplayName;
    MessageBox.Show(msg,
        "GetAccountForFolder",
        MessageBoxButtons.OK,
        MessageBoxIcon.Information);
}

Outlook.Account GetAccountForFolder(Outlook.Folder folder)
{
    // Obtain the store on which the folder resides.
    Outlook.Store store = folder.Store;

    // Enumerate the accounts defined for the session.
    foreach (Outlook.Account account in Application.Session.Accounts)
    {
        // Match the DefaultStore.StoreID of the account
        // with the Store.StoreID for the currect folder.
        if (account.DeliveryStore.StoreID  == store.StoreID)
        {
            // Return the account whose default delivery store
            // matches the store of the given folder.
            return account;
        }
     }
     // No account matches, so return null.
     return null;
}
```

## <a name="see-also"></a>関連項目

- [アカウント](accounts.md)

