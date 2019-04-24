---
title: 会議出席依頼への返信をユーザーに求める
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26e59cca7431e9f11f3fea5fa058548b9a5903a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320049"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a>会議出席依頼への返信をユーザーに求める

この例では、会議出席依頼への返信をユーザーに求める確認メッセージを表示し、ユーザーが送信の前に返信を編集できるようにする方法を説明します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

その後、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) メソッドを使用して、会議の開催者に、会議が承諾されたか、辞退されたか、受信者の予定表に暫定的に追加されたかを通知します。 **Respond** メソッドを使用すると、通知を自動的に送信するか、または送信する前にユーザーが返信を編集できるようにするかを、指定できます。 **Respond** メソッドは、3 つのパラメーターを受け取ります。 *Response* パラメーターは、応答が受諾、辞退、仮の予定のいずれであるかを示します。 *fNoUI* パラメーターと *fAdditionalTextDialog* パラメーターは、それぞれ、返信を開催者に送信するかどうか、および送信する前にユーザーが返信の本文を編集できるかどうかを示す **bool** 値です。 

次のコード例の PromptUserMeetingRequest では、[MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) オブジェクトを列挙して関連付けられた **AppointmentItem** オブジェクトを取得した後、*fNoUI* パラメーターを **false** に設定し、*fAdditionalTextDialog* パラメーターを **true** に設定して、**Respond** メソッドを呼び出します。 これにより、ユーザーは返信を送信するかどうか、送信する前に返信の本文を編集するかどうかを選択できます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
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
                false, true);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [会議出席依頼](meeting-requests.md)

