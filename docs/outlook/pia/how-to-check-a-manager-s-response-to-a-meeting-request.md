---
title: 会議出席依頼に対する上司からの返信を確認する
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b2e55037cf4d1d2ae4d153472b8f58a6e184b9e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619359"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a>会議出席依頼に対する上司からの返信を確認する

この例では、[GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドおよび [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを使用して、会議出席依頼に対する現在のユーザーの上司からの返信の状態を確認する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

ある受信者が会議出席依頼を承諾したか辞退したかを確認するには、[AppointmentItem](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) オブジェクトに関連付けられている [Recipients](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) コレクションから [Recipient](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) オブジェクトの [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) プロパティを使用します。

次のコード サンプルの CheckManagerResponseStatus は、パラメーターとして **AppointmentItem** オブジェクトを使用します。 CheckManagerResponseStatus では、現在のユーザーの **GetExchangeUser** メソッドを呼び出して [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを取得します。 次に、CheckManagerResponseStatus は **GetExchangeUserManager** メソッドを呼び出して、現在のユーザーの上司に関連付けられている **ExchangeUser** オブジェクトを取得します。 [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) メソッドを使用して、**AppointmentItem** に関連付けられている **Recipient** オブジェクトが、ユーザーの上司を表す **ExchangeUser** オブジェクトと同一であるかどうか確認します。 **CompareEntryIDs** が **true** を返す場合は、ユーザーの上司が **Recipients** コレクション内に存在し、CheckManagerResponseStatus は上司の **MeetingResponseStatus** を返します。 **CompareEntryIDs** が **false** を返す場合、CheckManagerResponseStatus は null 参照を返します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a>関連項目

- [Exchange ユーザー](exchange-users.md)

