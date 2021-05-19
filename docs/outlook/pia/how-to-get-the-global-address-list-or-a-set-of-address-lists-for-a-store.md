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
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a><span data-ttu-id="0597d-102">ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する</span><span class="sxs-lookup"><span data-stu-id="0597d-102">Get the Global Address List or a set of address lists for a store</span></span>

<span data-ttu-id="0597d-103">このトピックには、ストアに関連付けられたグローバル アドレス一覧 (GAL) を取得する方法、およびストアに関連付けられたすべてのアドレス一覧を取得する方法を示す 2 つのコード例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0597d-103">This topic contains two code examples that show how to get the Global Address List (GAL) that is associated with a store, and how to get all of the address lists that are associated with a store.</span></span>

## <a name="example"></a><span data-ttu-id="0597d-104">例</span><span class="sxs-lookup"><span data-stu-id="0597d-104">Example</span></span>

<span data-ttu-id="0597d-p101">複数の Exchange アカウントがプロファイルで定義されている Outlook セッションでは、複数のアドレス一覧がストアと関連付けられている場合があります。以下で示すどちらのコード例でも、対象になっている特定のストアは、アクティブなエクスプローラーに表示されている現在のフォルダーに対するストアですが、ストアに対するグローバル アドレス一覧または一連の [AddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist?redirectedfrom=MSDN&view=outlook-pia) オブジェクトを取得するためのアルゴリズムは、どのような Exchange ストアにも適用できます。</span><span class="sxs-lookup"><span data-stu-id="0597d-p101">In an Outlook session where multiple Exchange accounts are defined in the profile, there can be multiple address lists associated with a store. In each of the following code examples, the specific store of interest is the store for the current folder displayed in the active explorer, but the algorithm to get a Global Address List or a set of [AddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist?redirectedfrom=MSDN&view=outlook-pia) objects for a store applies to any Exchange store.</span></span>

<span data-ttu-id="0597d-107">1 番目のコード例には、DisplayGlobalAddressListForStore メソッドと GetGlobalAddressList 関数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0597d-107">The first code example contains the DisplayGlobalAddressListForStore method and the GetGlobalAddressList function.</span></span> <span data-ttu-id="0597d-108">DisplayGlobalAddressListForStore メソッドでは、現在のストアに関連付けられているグローバル アドレス一覧が [**名前の選択**] ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0597d-108">The DisplayGlobalAddressListForStore method displays, in the **Select Names** dialog box, the Global Address List that is associated with the current store.</span></span> <span data-ttu-id="0597d-109">最初に、DisplayGlobalAddressListForStore は現在のストアを取得します。</span><span class="sxs-lookup"><span data-stu-id="0597d-109">DisplayGlobalAddressListForStore first obtains the current store.</span></span> <span data-ttu-id="0597d-110">現在のストアが Exchange ストアの場合は、GetGlobalAddressList が呼び出され現在のストアに関連付けられているグローバル アドレス一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="0597d-110">If the current store is an Exchange store, GetGlobalAddressList is called to obtain the Global Address List associated with the current store.</span></span> 

<span data-ttu-id="0597d-111">GetGlobalAddressList は [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia) オブジェクトと MAPI プロパティ https://schemas.microsoft.com/mapi/proptag/0x3D150102 を使用してアドレス一覧と現在のストの PR\_EMSMDB\_SECTION\_UID プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="0597d-111">GetGlobalAddressList uses the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia) object and the MAPI property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list and the current store.</span></span> <span data-ttu-id="0597d-112">GetGlobalAddressList は、アドレス一覧とストアの PR\_EMSMDB\_SECTION \_UID プロパティが一致した場合にそのアドレス一覧がストアに関連付けられたものと識別します。[AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) プロパティが [ olExchangeGlobalAddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.oladdresslisttype?redirectedfrom=MSDN&view=outlook-pia) の場合、そのアドレス一覧はグローバル アドレス一覧となります。</span><span class="sxs-lookup"><span data-stu-id="0597d-112">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and the address list is the Global Address List if its [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) property is [olExchangeGlobalAddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.oladdresslisttype?redirectedfrom=MSDN&view=outlook-pia).</span></span> <span data-ttu-id="0597d-113">GetGlobalAddressList の呼び出しが成功すると、DisplayGlobalAddressListForStore は [SelectNamesDialog]( オブジェクトを使用して、[名前の選択] ダイアログ ボックスに返されるグローバル アドレス一覧を表示します。 https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.selectnamesdialog?redirectedfrom=MSDN&view=outlook-pia\) </span><span class="sxs-lookup"><span data-stu-id="0597d-113">If the call to GetGlobalAddressList succeeds, DisplayGlobalAddressListForStore uses the [SelectNamesDialog](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.selectnamesdialog?redirectedfrom=MSDN&view=outlook-pia\) object to display the returned Global Address List in the **Select Names** dialog box.</span></span>

<span data-ttu-id="0597d-114">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0597d-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0597d-115">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0597d-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0597d-116">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0597d-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

<span data-ttu-id="0597d-117">2 番目のコード例には、EnumerateAddressListsForStore メソッドと GetAddressLists 関数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0597d-117">The second code example contains the EnumerateAddressListsForStore method and GetAddressLists function.</span></span> <span data-ttu-id="0597d-118">EnumerateAddressListsForStore メソッドでは、現在のストアで定義された各アドレス一覧の種類と解決順序が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0597d-118">The EnumerateAddressListsForStore method displays the type and resolution order of each address list defined for the current store.</span></span> <span data-ttu-id="0597d-119">EnumerateAddressListsForStore はまず現在のストアを取得し、その後 GetAddressLists を呼び出して現在のストアの AddressList オブジェクトが格納されている .NET Framework の汎用 [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?redirectedfrom=MSDN&view=netframework-4.8)を取得します。</span><span class="sxs-lookup"><span data-stu-id="0597d-119">EnumerateAddressListsForStore first obtains the current store, and then calls GetAddressLists to obtain a .NET Framework generic [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?redirectedfrom=MSDN&view=netframework-4.8) object that contains AddressList objects for the current store.</span></span> 

<span data-ttu-id="0597d-120">GetAddressLists は本セッションで定義された各アドレス一覧を列挙し、PropertyAccessor オブジェクトと MAPI 名前付きプロパティ https://schemas.microsoft.com/mapi/proptag/0x3D150102 を使用してアドレス一覧の PR\_EMSMDB\_SECTION\_UID プロパティと現在のストアの PR\_EMSMDB\_SECTION\_UID プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="0597d-120">GetAddressLists enumerates each address list defined for the session, uses the PropertyAccessor object and the MAPI named property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list, and the PR\_EMSMDB\_SECTION\_UID property of a current store.</span></span> <span data-ttu-id="0597d-121">GetGlobalAddressList は、アドレス一覧とストアの PR\_EMSMDB\_SECTION\_UID プロパティが一致した場合にそのアドレス一覧がストアに関連付けられたものと識別し、現在のストアのアドレス一覧のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="0597d-121">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and returns a set of address lists for the current store.</span></span> <span data-ttu-id="0597d-122">その後、EnumerateAddressListsForStore は **AddressList** オブジェクトの [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) と [ResolutionOrder](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.resolutionorder?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_ResolutionOrder) プロパティを使用して、返された各アドレス一覧の種類と解決順序を表示します。</span><span class="sxs-lookup"><span data-stu-id="0597d-122">EnumerateAddressListsForStore then uses the [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) and [ResolutionOrder](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.resolutionorder?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_ResolutionOrder) properties of the **AddressList** object to display the type and resolution order for each returned address list.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="0597d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="0597d-123">See also</span></span>

- [<span data-ttu-id="0597d-124">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="0597d-124">Address book</span></span>](address-book.md)

