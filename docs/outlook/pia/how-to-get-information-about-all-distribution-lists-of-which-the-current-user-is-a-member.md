---
title: 現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ef170173111287efb3eb96ad0882b9fb50a1aa5b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629292"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a>現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する

この例では、[GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) メソッドを使用して、現在のユーザーがメンバーになっているすべての配布リストについての情報を取得します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次の例では、GetCurrentUserMembership で **GetMemberOfList** メソッドを呼び出して、Exchange ユーザーがメンバーになっているすべての配布リストの [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) コレクションを取得します。 このユーザーがどの配布リストのメンバーでもない場合、**GetMemberOfList** はカウントが 0 の **AddressEntries** コレクションを返します。 ユーザーがオンラインの場合にのみ **GetMemberOfList** は **AddressEntries** コレクションを返します。それ以外の場合、**GetMemberOfList** は null 参照を返します。 GetCurrentUserMembership では、現在の [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを返す [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) メソッドを使用して、ユーザーがオンラインかどうかをテストしています。 この例では、アドレス エントリの取得後に、ユーザーの各配布リストに関する情報を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [Exchange ユーザー](exchange-users.md)

