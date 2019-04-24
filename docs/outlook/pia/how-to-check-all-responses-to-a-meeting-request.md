---
title: 会議出席依頼へのすべての返信を調べる
TOCTitle: Check all responses to a meeting request
ms:assetid: ebe10e5a-7f04-447a-bfc1-aa8a726cb0b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184650(v=office.15)
ms:contentKeyID: 55119881
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89f3aa7037659bb29346bb70338d535cbbc200b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359718"
---
# <a name="check-all-responses-to-a-meeting-request"></a>会議出席依頼へのすべての返信を調べる

この例では、会議出席依頼に対する各受信者の返信の状態を確認する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード例の CheckAttendeeStatus では、会議出席依頼を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションを列挙し、各 [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトの [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) プロパティを調べます。 各 **Recipient** オブジェクトは、会議出席依頼の受信者を表します。 **MeetingResponseStatus** プロパティの値は、次の [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) 列挙値のいずれかです。

- [olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CheckAttendeeStatus()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find("[Subject]='Sales Strategy FY2007'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            switch (recip.MeetingResponseStatus)
            {
                case Outlook.OlResponseStatus.olResponseAccepted:
                    Debug.WriteLine("Accepted: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseTentative:
                    Debug.WriteLine("Tentative: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseDeclined:
                    Debug.WriteLine("Declined: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseOrganized:
                    Debug.WriteLine("Organizer: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNone:
                    Debug.WriteLine("None: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNotResponded:
                    Debug.WriteLine("Not responded: " + recip.Name);
                    break;
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [会議出席依頼](meeting-requests.md)

