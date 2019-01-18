---
title: プロファイルのアドレス一覧を表示する
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703721"
---
# <a name="display-the-address-lists-for-a-profile"></a>プロファイルのアドレス一覧を表示する

この例では、現在のプロファイルのアドレス一覧を表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

現在のプロファイルには、[AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) コレクションで表されたアドレス一覧が含まれます。 AddressLists コレクションのインスタンスを取得するには、 [NameSpace](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) オブジェクトの [AddressLists](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) プロパティを使用する必要があります。

次のコード例の EnumerateAddressLists は、最初に foreach ステートメントを使用して AddressLists コレクション内の各 [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) オブジェクトを列挙します。 次に、[Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\))、[ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\))、[IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\))、および [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) の各プロパティの値を含む文字列を作成します。 最後に、文字列を EnumerateAddressLists が [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。 これにより、現在のプロファイルの各アドレス一覧が表示されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>関連項目

- [アドレス帳](address-book.md)

