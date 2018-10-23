---
title: 会議出席依頼への返信をユーザーに求める
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b309252685363774d45ff6f74e581b9be86b042f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407591"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a><span data-ttu-id="a8326-102">会議出席依頼への返信をユーザーに求める</span><span class="sxs-lookup"><span data-stu-id="a8326-102">Prompt a user to respond to a meeting request</span></span>

<span data-ttu-id="a8326-103">この例では、会議出席依頼への返信をユーザーに求める確認メッセージを表示し、ユーザーが送信の前に返信を編集できるようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a8326-103">This example shows how to prompt the user for a response to a meeting request, and to enable the user to edit the response before sending it.</span></span>

## <a name="example"></a><span data-ttu-id="a8326-104">例</span><span class="sxs-lookup"><span data-stu-id="a8326-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a8326-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="a8326-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="a8326-106">その後、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) メソッドを使用して、会議の開催者に、会議が承諾されたか、辞退されたか、受信者の予定表に暫定的に追加されたかを通知します。</span><span class="sxs-lookup"><span data-stu-id="a8326-106">The [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is used to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient's calendar.</span></span> <span data-ttu-id="a8326-107">**Respond** メソッドを使用すると、通知を自動的に送信するか、または送信する前にユーザーが返信を編集できるようにするかを、指定できます。</span><span class="sxs-lookup"><span data-stu-id="a8326-107">By using the **Respond** method, you can indicate whether you want to send the notification automatically, or whether you want to allow the user to edit the response before sending it.</span></span> <span data-ttu-id="a8326-108">**Respond** メソッドは、3 つのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a8326-108">The **Respond** method accepts three parameters.</span></span> <span data-ttu-id="a8326-109">*Response* パラメーターは、応答が受諾、辞退、仮の予定のいずれであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="a8326-109">The  *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="a8326-110">*fNoUI* パラメーターと *fAdditionalTextDialog* パラメーターは、それぞれ、返信を開催者に送信するかどうか、および送信する前にユーザーが返信の本文を編集できるかどうかを示す **bool** 値です。</span><span class="sxs-lookup"><span data-stu-id="a8326-110">The  *fNoUI* and  *fAdditionalTextDialog* parameters are **bool** values that indicate whether the response will be sent to the organizer, and whether the user can edit the body of the response before sending it, respectively.</span></span> 

<span data-ttu-id="a8326-111">次のコード例の PromptUserMeetingRequest では、[MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) オブジェクトを列挙して関連付けられた **AppointmentItem** オブジェクトを取得した後、*fNoUI* パラメーターを **false** に設定し、*fAdditionalTextDialog* パラメーターを **true** に設定して、**Respond** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a8326-111">In the following code example,   enumerates through the MeetingItem objects to get the associated AppointmentItem objects, and then calls the Respond method with the  fNoUI parameter set to false and the  fAdditionalTextDialog parameter set to true.</span></span> <span data-ttu-id="a8326-112">これにより、ユーザーは返信を送信するかどうか、送信する前に返信の本文を編集するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a8326-112">This allows the user to choose whether to send a response, and whether to edit the body of the response before sending it.</span></span>

<span data-ttu-id="a8326-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8326-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="a8326-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8326-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="a8326-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a8326-115">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a8326-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8326-116">See also</span></span>

- [<span data-ttu-id="a8326-117">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="a8326-117">Meeting Requests</span></span>](meeting-requests.md)
