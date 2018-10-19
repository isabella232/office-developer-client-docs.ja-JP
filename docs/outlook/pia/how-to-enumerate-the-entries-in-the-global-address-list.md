---
title: グローバル アドレス一覧のエントリを列挙する
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f9e392710940a63f5d7723d303d5cf48569ad92f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407549"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a>グローバル アドレス一覧のエントリを列挙する

この例では、グローバル アドレス一覧 (GAL) に含まれる簡易メール転送プロトコル (SMTP) のプライマリ アドレスから最初の 100 件を列挙します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード例では、[AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトの SMTP アドレスを、 [GetExchangeUser()](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) メソッドまたは [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) メソッドの呼び出しで [ExchangeUser](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) オブジェクトまたは [ExchangeDistributionList](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) オブジェクトにキャストすることで取得します。 **AddressEntry** オブジェクトが Exchange ユーザーを表している場合、EnumerateGAL は **AddressEntry** オブジェクトのプロパティを公開する **ExchangeUser** オブジェクトを返します。 これらを公開するには、[JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\))、[Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\))、[Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\))、[BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\))、[PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) などの ExchangeUser プロパティを使用します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateGAL()
{
    Outlook.AddressList gal =
        Application.Session.GetGlobalAddressList();
    if (gal != null)
    {
        for (int i = 1; 
            i <= Math.Min(100, gal.AddressEntries.Count - 1); i++)
        {
            Outlook.AddressEntry addrEntry =
                gal.AddressEntries[i];
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                Outlook.ExchangeUser exchUser =
                    addrEntry.GetExchangeUser();
                Debug.WriteLine(exchUser.Name + " "
                    + exchUser.PrimarySmtpAddress);
            }
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeDistributionListAddressEntry)
            {
                Outlook.ExchangeDistributionList exchDL =
                    addrEntry.GetExchangeDistributionList();
                Debug.WriteLine(exchDL.Name + " "
                    + exchDL.PrimarySmtpAddress);
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

[アドレス帳](address-book.md)

