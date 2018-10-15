---
title: ストアを追加または削除する
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b0c8184d5e062d560614a8703494b673485866e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407038"
---
# <a name="add-or-remove-a-store"></a><span data-ttu-id="dffa9-102">ストアを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="dffa9-102">Add or remove a store</span></span>

<span data-ttu-id="dffa9-103">この例では、特定のプロファイルのストアを追加および削除する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="dffa9-103">This example shows how to add and remove a store in a given profile.</span></span>

## <a name="example"></a><span data-ttu-id="dffa9-104">例</span><span class="sxs-lookup"><span data-stu-id="dffa9-104">Example</span></span>

<span data-ttu-id="dffa9-105">次のコード サンプルでは、指定されたプロファイルのストアを追加および削除する方法を示します。それぞれ、[NameSpace](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) オブジェクトの [AddStoreEx](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) メソッドおよび [RemoveStore](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dffa9-105">This code sample shows how to add and remove a store in a specified profile, by calling the [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) method and the [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) method respectively on the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="dffa9-106">Outlook では、PST ストアの追加や削除はプログラムによってのみ行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dffa9-106">In Outlook, you can add or remove a PST store only programmatically.</span></span> <span data-ttu-id="dffa9-107">次のコード サンプルでは、Unicode ストアを追加し、.pst ファイルをユーザーの .pst ファイルの既定の場所である Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook に格納します。</span><span class="sxs-lookup"><span data-stu-id="dffa9-107">The following code sample adds a Unicode store and places the .pst file in the default location for user .pst files: Documents and SettingsUserName>\Local Settings\Application Data\Microsoft\Outlook.</span></span> <span data-ttu-id="dffa9-108">Local Settings フォルダーの下の Application Data フォルダーへのパスは、Environment.SpecialFolder.LocalApplicationData を使用して取得します。</span><span class="sxs-lookup"><span data-stu-id="dffa9-108">The code sample uses   to retrieve the path to the Application Data folder under the Local Settings folder.</span></span> <span data-ttu-id="dffa9-109">ストアを追加した後、コード サンプルではストアを削除します。</span><span class="sxs-lookup"><span data-stu-id="dffa9-109">Once the store has been added, the code sample removes the store.</span></span> <span data-ttu-id="dffa9-110">**RemoveStore** メソッドで [Store](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトを削除するには [Folder](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) オブジェクトが必要なので、 [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) コレクションを列挙し、 **Store** オブジェクトの [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) プロパティに基づいて、追加したばかりの **Store** オブジェクトを見つけます。</span><span class="sxs-lookup"><span data-stu-id="dffa9-110">Because the **RemoveStore** method requires a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to remove the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, it enumerates the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to find the **Store** object that has just been added based on the [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) property of the **Store** object.</span></span>

<span data-ttu-id="dffa9-p102">**RemoveStore** は、現在のプロファイルからのストアの削除のみを行います。ファイル システムから .pst ファイルを削除することはありません。</span><span class="sxs-lookup"><span data-stu-id="dffa9-p102">**RemoveStore** only removes the store from the current profile. It does not delete the .pst file from the file system.</span></span>

<span data-ttu-id="dffa9-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dffa9-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="dffa9-114">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dffa9-114">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="dffa9-115">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="dffa9-115">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dffa9-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="dffa9-116">See also</span></span>

- [<span data-ttu-id="dffa9-117">ストア</span><span class="sxs-lookup"><span data-stu-id="dffa9-117">Stores</span></span>](stores.md)

