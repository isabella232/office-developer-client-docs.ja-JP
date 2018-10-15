---
title: Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 8aa7093b26366f5aa47ce054b27eff04d48889b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405792"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a><span data-ttu-id="4cb2a-102">Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する</span><span class="sxs-lookup"><span data-stu-id="4cb2a-102">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>

<span data-ttu-id="4cb2a-103">この例では、既定の連絡先フォルダーに対応するアドレス帳を取得して、[ **名前の選択**] ダイアログ ボックスにアドレス帳を表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-103">This example shows how to obtain the address book that corresponds to the default Contacts folder, and then displays the address book in the **Select Names** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="4cb2a-104">例</span><span class="sxs-lookup"><span data-stu-id="4cb2a-104">Example</span></span>

<span data-ttu-id="4cb2a-p101">Outlook では、すべてのアドレス帳は [NameSpace](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) オブジェクトの [AddressLists](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) プロパティのコレクションとして表されます。このコード サンプルでは、 [AddressList](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) オブジェクトの [GetContactsFolder](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) メソッドを使用して、各アドレス一覧に対応する連絡先フォルダーを検索します。Outlook の各フォルダーにはエントリ ID があります。既定の連絡先フォルダーのエントリ ID と連絡先フォルダーのエントリ ID を比較して、既定の連絡先フォルダーに対応する AddressList を生成します。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-p101">All address books in Outlook are represented as a collection by the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object. The code sample uses the [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) method of the [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object to find the contact folder that corresponds to each address list. Each Outlook folder has an Entry ID. Compare the Entry ID of the default Contacts folder with the Entry ID of a Contacts folder to produce the AddressList that corresponds to the default Contacts folder.</span></span>

<span data-ttu-id="4cb2a-109">既定の連絡先フォルダーに対応アドレス一覧を [ **名前の選択**] ダイアログ ボックスに表示する前に、コード サンプルではそのアドレス一覧を [SelectNamesDialog](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) オブジェクトの [InitialAddressList](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) プロパティの値として設定しています。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-109">Before displaying the address list corresponding to the default Contacts folder in the **Select Names** dialog box, the code sample sets it as the value of the [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) property of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object.</span></span>

<span data-ttu-id="4cb2a-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="4cb2a-111">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="4cb2a-112">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ShowContactsFolderAsInitialAddressList()
    Dim addrLists As Outlook.AddressLists
    Dim contactsFolder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts), _
        Outlook.Folder)
    addrLists = Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        Dim testFolder As Outlook.Folder = _
        CType(addrList.GetContactsFolder(), Outlook.Folder)
        If Not (testFolder Is Nothing) Then
            ' Test to determine if Folder returned
            ' by GetContactsFolder has same EntryID
            ' as default Contacts folder.
            If (Application.Session.CompareEntryIDs( _
                contactsFolder.EntryID, testFolder.EntryID)) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.InitialAddressList = addrList
                snd.Display()
            End If
        End If
    Next
End Sub
```


```csharp
private void ShowContactsFolderAsInitialAddressList()
{
    Outlook.AddressLists addrLists;
    Outlook.Folder contactsFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    addrLists = Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        Outlook.Folder testFolder =
            addrList.GetContactsFolder() as Outlook.Folder;
        if (testFolder != null)
        {
            // Test to determine if Folder returned
            // by GetContactsFolder has same EntryID
            // as default Contacts folder.
            if (Application.Session.CompareEntryIDs(
                contactsFolder.EntryID, testFolder.EntryID))
            {
                Outlook.SelectNamesDialog snd =
                    Application.
                    Session.GetSelectNamesDialog();
                snd.InitialAddressList = addrList;
                snd.Display();
             }
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4cb2a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cb2a-113">See also</span></span>

- [<span data-ttu-id="4cb2a-114">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="4cb2a-114">Address Book</span></span>](address-book.md)

