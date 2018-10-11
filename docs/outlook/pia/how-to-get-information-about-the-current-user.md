---
title: 現在のユーザーの情報を取得する
TOCTitle: Get information about the current user
ms:assetid: 3802523a-3ccf-4cca-a348-abe2645a0d9c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184601(v=office.15)
ms:contentKeyID: 55119840
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7ac10c01d205f4f4590183bcef8006e8f1344cbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406975"
---
# <a name="get-information-about-the-current-user"></a>現在のユーザーの情報を取得する

この例では、現在のユーザーの情報 (名前、役職、電話番号など) を取得する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトから取得するには、**AddressEntry** オブジェクトの [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドを呼び出します。 次のプロシージャで GetCurrentUserInfo は、[CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) プロパティを使用して、[Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトの [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) プロパティを取得します。 **AddressEntry** オブジェクトが Exchange メールボックス ユーザーを表している場合、GetCurrentUserInfo は **GetExchangeUser** メソッドを呼び出し、**ExchangeUser** オブジェクトが返されます。 [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\))、[PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\))、[JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\))、[Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\))、[OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\))、[BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\))、および [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) の各プロパティが、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き出されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserInfo()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser currentUser =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser();
        if (currentUser != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + currentUser.Name);
            sb.AppendLine("STMP address: "
                + currentUser.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + currentUser.JobTitle);
            sb.AppendLine("Department: "
                + currentUser.Department);
            sb.AppendLine("Location: "
                + currentUser.OfficeLocation);
            sb.AppendLine("Business phone: "
                + currentUser.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + currentUser.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [Exchange ユーザー](exchange-users.md)

