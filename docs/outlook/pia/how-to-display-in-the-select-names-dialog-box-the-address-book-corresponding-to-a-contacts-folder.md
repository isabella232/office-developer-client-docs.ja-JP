---
title: Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3be678b13738fead1509f3854c7b23bd0cfc8528
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699220"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a>Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する

この例では、既定の連絡先フォルダーに対応するアドレス帳を取得して、[ **名前の選択**] ダイアログ ボックスにアドレス帳を表示する方法を示します。

## <a name="example"></a>例

Outlook では、すべてのアドレス帳は [NameSpace](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) オブジェクトの [AddressLists](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) プロパティのコレクションとして表されます。このコード サンプルでは、 [AddressList](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) オブジェクトの [GetContactsFolder](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) メソッドを使用して、各アドレス一覧に対応する連絡先フォルダーを検索します。Outlook の各フォルダーにはエントリ ID があります。既定の連絡先フォルダーのエントリ ID と連絡先フォルダーのエントリ ID を比較して、既定の連絡先フォルダーに対応する AddressList を生成します。

既定の連絡先フォルダーに対応アドレス一覧を [ **名前の選択**] ダイアログ ボックスに表示する前に、コード サンプルではそのアドレス一覧を [SelectNamesDialog](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) オブジェクトの [InitialAddressList](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) プロパティの値として設定しています。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [アドレス帳](address-book.md)

