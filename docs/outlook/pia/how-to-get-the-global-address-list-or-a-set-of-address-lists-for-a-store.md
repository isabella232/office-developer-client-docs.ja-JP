---
title: ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 582b0e836edc361d1d8717f94a5d7490c57cd530
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719465"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する

このトピックには、ストアに関連付けられたグローバル アドレス一覧 (GAL) を取得する方法、およびストアに関連付けられたすべてのアドレス一覧を取得する方法を示す 2 つのコード例が含まれます。

## <a name="example"></a>例

複数の Exchange アカウントがプロファイルで定義されている Outlook セッションでは、複数のアドレス一覧がストアと関連付けられている場合があります。以下で示すどちらのコード例でも、対象になっている特定のストアは、アクティブなエクスプローラーに表示されている現在のフォルダーに対するストアですが、ストアに対するグローバル アドレス一覧または一連の [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) オブジェクトを取得するためのアルゴリズムは、どのような Exchange ストアにも適用できます。

1 番目のコード例には、DisplayGlobalAddressListForStore メソッドと GetGlobalAddressList 関数が含まれています。 DisplayGlobalAddressListForStore メソッドでは、現在のストアに関連付けられているグローバル アドレス一覧が [**名前の選択**] ダイアログ ボックスに表示されます。 最初に、DisplayGlobalAddressListForStore は現在のストアを取得します。 現在のストアが Exchange ストアの場合は、GetGlobalAddressList が呼び出され現在のストアに関連付けられているグローバル アドレス一覧を取得します。 

GetGlobalAddressList は [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトと MAPI プロパティ https://schemas.microsoft.com/mapi/proptag/0x3D150102 を使用してアドレス一覧と現在のストの PR\_EMSMDB\_SECTION\_UID プロパティを取得します。 GetGlobalAddressList は、アドレス一覧とストアの PR\_EMSMDB\_SECTION \_UID プロパティが一致した場合にそのアドレス一覧がストアに関連付けられたものと識別します。[AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) プロパティが [ olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)) の場合、そのアドレス一覧はグローバル アドレス一覧となります。 GetGlobalAddressList への呼び出しが成功した場合、DisplayGlobalAddressListForStore は [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) オブジェクトを使用して、返されたグローバル アドレス一覧を [**名前の選択**] ダイアログ ボックスに表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
void DisplayGlobalAddressListForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    if (currentStore.ExchangeStoreType !=
        Outlook.OlExchangeStoreType.olNotExchange)
    {
        Outlook.SelectNamesDialog snd = 
            Application.Session.GetSelectNamesDialog();
        Outlook.AddressList addrList = 
            GetGlobalAddressList(currentStore);
        if (addrList != null)
        {
            snd.InitialAddressList = addrList;
            snd.Display();
        }
    }
}

public Outlook.AddressList GetGlobalAddressList(Outlook.Store store)
{
    string  PR_EMSMDB_SECTION_UID = 
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList 
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList = 
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID && addrList.AddressListType ==
            Outlook.OlAddressListType.olExchangeGlobalAddressList)
        {
            return addrList;
        }
    }
    return null;
}
```

2 番目のコード例には、EnumerateAddressListsForStore メソッドと GetAddressLists 関数が含まれています。 EnumerateAddressListsForStore メソッドでは、現在のストアで定義された各アドレス一覧の種類と解決順序が表示されます。 EnumerateAddressListsForStore はまず現在のストアを取得し、その後 GetAddressLists を呼び出して現在のストアの AddressList オブジェクトが格納されている .NET Framework の汎用 [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19)を取得します。 

GetAddressLists は本セッションで定義された各アドレス一覧を列挙し、PropertyAccessor オブジェクトと MAPI 名前付きプロパティ https://schemas.microsoft.com/mapi/proptag/0x3D150102 を使用してアドレス一覧の PR\_EMSMDB\_SECTION\_UID プロパティと現在のストアの PR\_EMSMDB\_SECTION\_UID プロパティを取得します。 GetGlobalAddressList は、アドレス一覧とストアの PR\_EMSMDB\_SECTION\_UID プロパティが一致した場合にそのアドレス一覧がストアに関連付けられたものと識別し、現在のストアのアドレス一覧のセットを返します。 その後、EnumerateAddressListsForStore は **AddressList** オブジェクトの [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) と [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) プロパティを使用して、返された各アドレス一覧の種類と解決順序を表示します。

```csharp
private void EnumerateAddressListsForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    List<Outlook.AddressList> addrListsForStore = 
        GetAddressLists(currentStore);
    foreach (Outlook.AddressList addrList in addrListsForStore)
    {
        Debug.WriteLine(addrList.Name 
            + " " + addrList.AddressListType.ToString()
            + " Resolution Order: " +
            addrList.ResolutionOrder);
    }
}
public List<Outlook.AddressList> GetAddressLists(Outlook.Store store)
{
    List<Outlook.AddressList> addrLists = 
        new List<Microsoft.Office.Interop.Outlook.AddressList>();
    string PR_EMSMDB_SECTION_UID =
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList =
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID)
        {
            addrLists.Add(addrList);
        }
    }
    return addrLists;
}
```

## <a name="see-also"></a>関連項目

- [アドレス帳](address-book.md)

