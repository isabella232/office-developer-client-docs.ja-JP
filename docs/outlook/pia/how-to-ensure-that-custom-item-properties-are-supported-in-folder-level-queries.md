---
title: フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcba2648988d2de3c208079d2845e2cb4c2f549
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319090"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a>フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする

この例では、あるアイテム型にカスタム プロパティを追加した場合に、フォルダーにもそのプロパティを追加して、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。

## <a name="example"></a>例

このサンプル コードは、あるアイテム型にカスタム プロパティを追加した場合に、[UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) オブジェクトと [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) オブジェクトを使用してフォルダーにもそのプロパティを追加し、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。

[UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) コレクションの [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) メソッドを使用してアイテムにカスタム プロパティを追加するときに、*AddToFolderFields* パラメーターに **true** を指定すると、フォルダーにプロパティを追加できます。 ただし、開発者の間違いやユーザーの操作により (Outlook の [フィールドの選択] からカスタム プロパティを削除した場合や、アイテムを別のフォルダーに移動した場合など)、カスタム プロパティが目的のフォルダーに追加されないことがあります。 その結果として、そのカスタム プロパティを使用する [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) オブジェクトの [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) メソッドと [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) メソッドが失敗します。 **UserDefinedProperties** オブジェクトを使用すると、フォルダーにカスタム プロパティがあるかどうかをテストして、カスタム プロパティが存在しない場合や削除されていた場合は、カスタム プロパティを追加できます。

フォルダー内の **UserDefinedProperty** オブジェクトで表されるカスタム プロパティに値を保持するには、アイテムの同じ名前のカスタム プロパティに値を保存する必要があります。フォルダーの **UserDefinedProperty** オブジェクトに値を格納しても効果はありません。アイテムの **UserProperties** コレクションから目的の [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) オブジェクトにアクセスし、次にその **UserProperty** オブジェクトに値を設定します。この変更を保持するために、アイテムの **Save** メソッドを必ず呼び出してください。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [フォルダー](folders.md)

