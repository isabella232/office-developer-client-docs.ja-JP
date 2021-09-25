---
title: 会議出席依頼を自動的に承諾する
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d19963814e86587e3ad5b53071d43e647b596a88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590843"
---
# <a name="automatically-accept-a-meeting-request"></a>会議出席依頼を自動的に承諾する

この例では、[Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) メソッドを使用して自動的に会議出席依頼を承諾する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


[MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) オブジェクトは、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトで表される予定を受信者の予定表に追加する要求を表します。 会議出席依頼に応答するために、[GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) メソッドを使用して、その会議出席依頼に関連付けられた **AppointmentItem** を取得します。 その後、**AppointmentItem** の [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) メソッドを使用して、会議の開催者に、会議が承諾されたか、辞退されたか、受信者の予定表に暫定的に追加されたかを通知します。 **Respond** メソッドは、3 つのパラメーターを受け取ります。 

*Response* パラメーターは、応答が受諾、辞退、仮の予定のいずれであるかを示します。 fNoUI と fAdditionalTextDialog は **bool** 値のパラメーターで、それぞれ、応答を送信するかどうか、ユーザーが応答を編集できるかどうかを決定します。 次のコード例の AutoAcceptMeetingRequests では、すべての **MeetingItem** オブジェクトを列挙して、関連する **AppointmentItem** を取得します。 その後、AutoAcceptMeetingRequests では、*fNoUI* パラメーターを指定した **Respond** メソッドを使用します。このパラメーターは、会議出席依頼を受諾する応答を自動的に送信するように指示するために **true** に設定します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [会議出席依頼](meeting-requests.md)

