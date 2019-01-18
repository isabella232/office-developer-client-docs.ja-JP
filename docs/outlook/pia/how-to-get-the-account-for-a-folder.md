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
# <a name="get-the-account-for-a-folder"></a><span data-ttu-id="508b0-102">フォルダーのアカウントを取得する</span><span class="sxs-lookup"><span data-stu-id="508b0-102">Get the account for a folder</span></span>

<span data-ttu-id="508b0-103">この例では、現在のセッションで特定のフォルダーに関連付けられているアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="508b0-103">This example gets the account that is associated with a folder in the current session.</span></span>

## <a name="example"></a><span data-ttu-id="508b0-104">例</span><span class="sxs-lookup"><span data-stu-id="508b0-104">Example</span></span>

<span data-ttu-id="508b0-105">以下のコード例の DisplayAccountForCurrentFolder 関数は GetAccountForFolder 関数を呼び出して、現在のフォルダーをホストしている既定の配信ストアのアカウントを特定し、そのフォルダーの名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="508b0-105">In the following code example, the DisplayAccountForCurrentFolder function calls the GetAccountForFolder function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.</span></span> <span data-ttu-id="508b0-106">GetAccountForFolder は、現在のフォルダーのストア ([Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) プロパティから取得) を、セッションの [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) コレクションで定義されている各アカウントの既定の配信ストア ([DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) プロパティで取得) と照合します。</span><span class="sxs-lookup"><span data-stu-id="508b0-106">GetAccountForFolder matches the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="508b0-107">GetAccountForFolder は、一致するものが見つかった場合は [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを返し、見つからなかった場合は Null 参照を返します。</span><span class="sxs-lookup"><span data-stu-id="508b0-107">GetAccountForFolder returns the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object if a match is found; otherwise, it returns a null reference.</span></span>

<span data-ttu-id="508b0-p102">Microsoft Outlook セッションでプロファイルに複数のアカウントが定義されているとき、アクティブなエクスプローラーに表示されるフォルダーは、そのセッションの既定のストアには必ずしも存在せず、複数のアカウントに関連付けられた複数のストアのいずれかに存在します。このトピックでは、既定の配信ストアがフォルダーをホストしているストアでもあるときに、そのアカウントを特定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="508b0-p102">In a Microsoft Outlook session that has multiple accounts defined in the profile, the folder that is displayed in the active explorer does not necessarily reside on the default store for that session; instead, it can reside on one of the multiple stores associated with the multiple accounts. This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span>

<span data-ttu-id="508b0-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="508b0-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="508b0-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="508b0-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="508b0-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="508b0-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="508b0-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="508b0-113">See also</span></span>

- [<span data-ttu-id="508b0-114">アカウント</span><span class="sxs-lookup"><span data-stu-id="508b0-114">Accounts</span></span>](accounts.md)

