---
title: Exchange 配布リストのメンバーを取得する
TOCTitle: Get members of an Exchange distribution list
ms:assetid: 75b38e40-772c-400b-8df9-e3e385b87f9c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb645998(v=office.15)
ms:contentKeyID: 55119837
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 730ef62b6bff9cbfc2bf4aaae51116d2fe026131
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406562"
---
# <a name="get-members-of-an-exchange-distribution-list"></a><span data-ttu-id="cdeb8-102">Exchange 配布リストのメンバーを取得する</span><span class="sxs-lookup"><span data-stu-id="cdeb8-102">Get members of an Exchange distribution list</span></span>

<span data-ttu-id="cdeb8-103">この例では、ユーザーが [ **名前の選択**] ダイアログ ボックスで Exchange の配布リストを選択できるようにし、配布リストを展開してメンバーを表示します。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-103">This example prompts the user to select an Exchange distribution list from the **Select Names** dialog box and expands the distribution list to display its members.</span></span>

## <a name="example"></a><span data-ttu-id="cdeb8-104">例</span><span class="sxs-lookup"><span data-stu-id="cdeb8-104">Example</span></span>

<span data-ttu-id="cdeb8-p101">このコード サンプルでは、[ExchangeDistributionList](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) オブジェクトの [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) メソッドを呼び出して、リストのすべてのメンバーが格納されている [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) コレクションを取得します。配布リストは別の配布リストの中に入れ子にできるので、返される **AddressEntries** コレクションは任意の型の Exchange [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-p101">This code sample calls the [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) method of the [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that contains all the members of the list. Because distribution lists can be nested inside another distribution list, the returned **AddressEntries** collection can represent any type of Exchange [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span>


> [!NOTE]
> <span data-ttu-id="cdeb8-p102">[!メモ] 配布リストを展開すると Exchange サーバーのパフォーマンスに負荷がかかる場合があるので、 **GetExchangeDistributionListMembers** メソッドの使用には注意が必要です。大きい配布リストを展開するときは、コードの動作が遅くなるものと考えてください。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-p102">Expanding distribution lists can create a performance burden on an Exchange server, so use the **GetExchangeDistributionListMembers** method cautiously. Expect that your code will be slow when it expands large distribution lists.</span></span>

<span data-ttu-id="cdeb8-109">配布リストのメンバーを取得するには、ユーザーが Exchange サーバーに接続し、オンライン状態になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-109">To obtain the members of a distribution list, the user must be connected to an Exchange server and online.</span></span>

<span data-ttu-id="cdeb8-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="cdeb8-111">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="cdeb8-112">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cdeb8-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetDistributionListMembers()
    Dim snd As Outlook.SelectNamesDialog = _
        Application.Session.GetSelectNamesDialog()
    Dim addrLists As Outlook.AddressLists = _
        Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        If addrList.Name = "All Groups" Then
            snd.InitialAddressList = addrList
            Exit For
        End If
    Next
    snd.NumberOfRecipientSelectors = _
        Outlook.OlRecipientSelectors.olShowTo
    snd.ToLabel = "D/L"
    snd.ShowOnlyInitialAddressList = True
    snd.AllowMultipleSelection = False
    snd.Display()
    If (snd.Recipients.Count > 0) Then
        Dim addrEntry As Outlook.AddressEntry = _
            snd.Recipients(1).AddressEntry
        If (addrEntry.AddressEntryUserType = _
            Outlook.OlAddressEntryUserType. _
            olExchangeDistributionListAddressEntry) Then
            Dim exchDL As Outlook.ExchangeDistributionList = _
                addrEntry.GetExchangeDistributionList()
            Dim addrEntries As Outlook.AddressEntries = _
                exchDL.GetExchangeDistributionListMembers()
            If Not (addrEntries Is Nothing) Then
                For Each exchDLMember As _
                    Outlook.AddressEntry In addrEntries
                    Debug.WriteLine(exchDLMember.Name)
                Next
            End If
         End If
    End If
End Sub
```


```csharp
private void GetDistributionListMembers()
{
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    Outlook.AddressLists addrLists =
        Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        if (addrList.Name == "All Groups")
        {
            snd.InitialAddressList = addrList;
            break;
        }
    }
    snd.NumberOfRecipientSelectors =
        Outlook.OlRecipientSelectors.olShowTo;
    snd.ToLabel = "D/L";
    snd.ShowOnlyInitialAddressList = true;
    snd.AllowMultipleSelection = false;
    snd.Display();
    if (snd.Recipients.Count > 0)
    {
        Outlook.AddressEntry addrEntry =
            snd.Recipients[1].AddressEntry;
        if (addrEntry.AddressEntryUserType ==
            Outlook.OlAddressEntryUserType.
            olExchangeDistributionListAddressEntry)
        {
            Outlook.ExchangeDistributionList exchDL =
                addrEntry.GetExchangeDistributionList();
            Outlook.AddressEntries addrEntries =
                exchDL.GetExchangeDistributionListMembers();
            if (addrEntries != null)
                foreach (Outlook.AddressEntry exchDLMember
                    in addrEntries)
                {
                    Debug.WriteLine(exchDLMember.Name);
                }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="cdeb8-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdeb8-113">See also</span></span>

- [<span data-ttu-id="cdeb8-114">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="cdeb8-114">Exchange Users</span></span>](exchange-users.md)

