---
title: ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store
ms:contentKeyID: 55119800
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f0f7ba9b8854603646dc41e1017c2465c4af2d8
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819330"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する

このトピックには、ストアに関連付けられたグローバル アドレス一覧 (GAL) を取得する方法、およびストアに関連付けられたすべてのアドレス一覧を取得する方法を示す 2 つのコード例が含まれます。

## <a name="example"></a>例

複数の Exchange アカウントがプロファイルで定義されている Outlook セッションでは、複数のアドレス一覧がストアと関連付けられている場合があります。以下で示すどちらのコード例でも、対象になっている特定のストアは、アクティブなエクスプローラーに表示されている現在のフォルダーに対するストアですが、ストアに対するグローバル アドレス一覧または一連の [AddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist?redirectedfrom=MSDN&view=outlook-pia) オブジェクトを取得するためのアルゴリズムは、どのような Exchange ストアにも適用できます。

1 番目のコード例には、DisplayGlobalAddressListForStore メソッドと GetGlobalAddressList 関数が含まれています。 DisplayGlobalAddressListForStore メソッドでは、現在のストアに関連付けられているグローバル アドレス一覧が [**名前の選択**] ダイアログ ボックスに表示されます。 最初に、DisplayGlobalAddressListForStore は現在のストアを取得します。 現在のストアが Exchange ストアの場合は、GetGlobalAddressList が呼び出され現在のストアに関連付けられているグローバル アドレス一覧を取得します。 

GetGlobalAddressList は [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia) オブジェクトと MAPI プロパティ https://schemas.microsoft.com/mapi/proptag/0x3D150102 を使用してアドレス一覧と現在のストの PR\_EMSMDB\_SECTION\_UID プロパティを取得します。 GetGlobalAddressList は、アドレス一覧とストアの PR\_EMSMDB\_SECTION \_UID プロパティが一致した場合にそのアドレス一覧がストアに関連付けられたものと識別します。[AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) プロパティが [ olExchangeGlobalAddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.oladdresslisttype?redirectedfrom=MSDN&view=outlook-pia) の場合、そのアドレス一覧はグローバル アドレス一覧となります。 GetGlobalAddressList の呼び出しが成功すると、DisplayGlobalAddressListForStore は [SelectNamesDialog] (https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.selectnamesdialog?redirectedfrom=MSDN&view=outlook-pia\)オブジェクト) を使用して、返されたグローバルアドレス一覧を [**名前の選択**] ダイアログボックスに表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

2 番目のコード例には、EnumerateAddressListsForStore メソッドと GetAddressLists 関数が含まれています。 EnumerateAddressListsForStore メソッドでは、現在のストアで定義された各アドレス一覧の種類と解決順序が表示されます。 EnumerateAddressListsForStore はまず現在のストアを取得し、その後 GetAddressLists を呼び出して現在のストアの AddressList オブジェクトが格納されている .NET Framework の汎用 [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?redirectedfrom=MSDN&view=netframework-4.8)を取得します。 

GetAddressLists は本セッションで定義された各アドレス一覧を列挙し、PropertyAccessor オブジェクトと MAPI 名前付きプロパティ https://schemas.microsoft.com/mapi/proptag/0x3D150102 を使用してアドレス一覧の PR\_EMSMDB\_SECTION\_UID プロパティと現在のストアの PR\_EMSMDB\_SECTION\_UID プロパティを取得します。 GetGlobalAddressList は、アドレス一覧とストアの PR\_EMSMDB\_SECTION\_UID プロパティが一致した場合にそのアドレス一覧がストアに関連付けられたものと識別し、現在のストアのアドレス一覧のセットを返します。 その後、EnumerateAddressListsForStore は **AddressList** オブジェクトの [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) と [ResolutionOrder](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.resolutionorder?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_ResolutionOrder) プロパティを使用して、返された各アドレス一覧の種類と解決順序を表示します。


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
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

