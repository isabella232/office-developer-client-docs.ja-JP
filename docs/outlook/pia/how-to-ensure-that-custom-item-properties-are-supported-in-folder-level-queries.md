---
title: フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 659919de8eeb17e675ed67f3b777f67b04f13b54
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406940"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a><span data-ttu-id="47077-102">フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする</span><span class="sxs-lookup"><span data-stu-id="47077-102">Ensure that custom item properties are supported in folder-level queries</span></span>

<span data-ttu-id="47077-103">この例では、あるアイテム型にカスタム プロパティを追加した場合に、フォルダーにもそのプロパティを追加して、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="47077-103">This example shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

## <a name="example"></a><span data-ttu-id="47077-104">例</span><span class="sxs-lookup"><span data-stu-id="47077-104">Example</span></span>

<span data-ttu-id="47077-105">このサンプル コードは、あるアイテム型にカスタム プロパティを追加した場合に、[UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) オブジェクトと [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) オブジェクトを使用してフォルダーにもそのプロパティを追加し、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="47077-105">This code sample shows how to use the [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) object and the [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) object to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

<span data-ttu-id="47077-106">[UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) コレクションの [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) メソッドを使用してアイテムにカスタム プロパティを追加するときに、*AddToFolderFields* パラメーターに **true** を指定すると、フォルダーにプロパティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="47077-106">When you use the [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) method on the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection to add a custom property to an item, you can specify the *AddToFolderFields* parameter as **true** to add the property to the folder.</span></span> <span data-ttu-id="47077-107">ただし、開発者の間違いやユーザーの操作により (Outlook の [フィールドの選択] からカスタム プロパティを削除した場合や、アイテムを別のフォルダーに移動した場合など)、カスタム プロパティが目的のフォルダーに追加されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="47077-107">However, the custom property might not get added to the desired folderbecause of developer error or a user action, such as removing the custom property through the Outlook Field Chooser or moving the item to another folder.</span></span> <span data-ttu-id="47077-108">その結果として、そのカスタム プロパティを使用する [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) オブジェクトの [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) メソッドと [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) メソッドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="47077-108">Consequently, the [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) method and the [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) object that uses that custom property will fail.</span></span> <span data-ttu-id="47077-109">**UserDefinedProperties** オブジェクトを使用すると、フォルダーにカスタム プロパティがあるかどうかをテストして、カスタム プロパティが存在しない場合や削除されていた場合は、カスタム プロパティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="47077-109">By using the **UserDefinedProperties** object, you can test whether your custom properties exist in the folder, and add the custom properties if they do not exist or if they have been removed.</span></span>

<span data-ttu-id="47077-p102">フォルダー内の **UserDefinedProperty** オブジェクトで表されるカスタム プロパティに値を保持するには、アイテムの同じ名前のカスタム プロパティに値を保存する必要があります。フォルダーの **UserDefinedProperty** オブジェクトに値を格納しても効果はありません。アイテムの **UserProperties** コレクションから目的の [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) オブジェクトにアクセスし、次にその **UserProperty** オブジェクトに値を設定します。この変更を保持するために、アイテムの **Save** メソッドを必ず呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="47077-p102">To persist a custom property represented by a **UserDefinedProperty** object in a folder, you must save the custom property with the same name in the item. Storing a value in the **UserDefinedProperty** object for the folder has no effect. You must se the item's **UserProperties** collection to access the [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) object that you want to set, and then set the value on the **UserProperty** object. Be sure to call the **Save** method on the item to persist your changes.</span></span>

<span data-ttu-id="47077-114">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="47077-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="47077-115">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47077-115">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="47077-116">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="47077-116">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoUserDefinedProperty()
    Dim folder As Outlook.Folder = _
        CType(Application.ActiveExplorer().CurrentFolder(), _
        Outlook.Folder)
    Dim post As Outlook.PostItem = CType( _
        folder.Items.Add("IPM.Post"), Outlook.PostItem)
    ' Add UserProperty to PostItem
    post.UserProperties.Add("ColorID", _
        Outlook.OlUserPropertyType.olText, False)
    post.UserProperties("ColorID").Value = "Green"
    post.Subject = "UserProperty Example"
    post.Save()
    Dim findPost As Outlook.PostItem
    Try
        ' Items.Find will fail unless custom property
        ' is defined in the folder
        findPost = _
            CType(folder.Items.Find("[ColorID] = 'Green'"), _
            Outlook.PostItem)
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
        ' Add ColorID field to the folder
        folder.UserDefinedProperties.Add("ColorID", _
            Outlook.OlUserPropertyType.olText)
        ' Now the find works ok
        Dim findPostOK As Outlook.PostItem
        Try
            findPostOK = _
                CType(folder.Items.Find("[ColorID] = 'Green'"), _
                Outlook.PostItem)
            If Not (findPostOK Is Nothing) Then
                Debug.WriteLine("Found PostItem")
            End If
            ' Cleanup by deleting PostItem and ColorID
            findPostOK.Delete()
            Dim userProperty As Outlook.UserDefinedProperty = _
                folder.UserDefinedProperties("ColorID")
            userProperty.Delete()
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
End Sub
```


```csharp
private void DemoUserDefinedProperty()
{
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.PostItem post = folder.Items.Add("IPM.Post")
        as Outlook.PostItem;
    // Add UserProperty to PostItem
    post.UserProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        false, Type.Missing);
    post.UserProperties["ColorID"].Value = "Green";
    post.Subject = "UserProperty Example";
    post.Save();
    Outlook.PostItem findPost;
    try
    {
        // Items.Find will fail unless custom property
        // is defined in the folder
        findPost =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
     // Add ColorID field to the folder
    folder.UserDefinedProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        Type.Missing, Type.Missing);
    // Now the find works ok
    Outlook.PostItem findPostOK;
    try
    {
        findPostOK =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
        if (findPostOK != null)
        {
            Debug.WriteLine("Found PostItem");
        }
        // Cleanup by deleting PostItem and ColorID
        findPostOK.Delete();
        Outlook.UserDefinedProperty userProperty =
            folder.UserDefinedProperties["ColorID"];
        userProperty.Delete();
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="47077-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="47077-117">See also</span></span>

- [<span data-ttu-id="47077-118">フォルダー</span><span class="sxs-lookup"><span data-stu-id="47077-118">Folders</span></span>](folders.md)

