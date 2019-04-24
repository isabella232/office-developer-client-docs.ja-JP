---
title: 会議出席依頼を自動的に承諾する
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359704"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="45acb-102">会議出席依頼を自動的に承諾する</span><span class="sxs-lookup"><span data-stu-id="45acb-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="45acb-103">この例では、[Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) メソッドを使用して自動的に会議出席依頼を承諾する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="45acb-103">This example shows how to use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="45acb-104">例</span><span class="sxs-lookup"><span data-stu-id="45acb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="45acb-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="45acb-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="45acb-106">[MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) オブジェクトは、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトで表される予定を受信者の予定表に追加する要求を表します。</span><span class="sxs-lookup"><span data-stu-id="45acb-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="45acb-107">会議出席依頼に応答するために、[GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) メソッドを使用して、その会議出席依頼に関連付けられた **AppointmentItem** を取得します。</span><span class="sxs-lookup"><span data-stu-id="45acb-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="45acb-108">その後、**AppointmentItem** の [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) メソッドを使用して、会議の開催者に、会議が承諾されたか、辞退されたか、受信者の予定表に暫定的に追加されたかを通知します。</span><span class="sxs-lookup"><span data-stu-id="45acb-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="45acb-109">**Respond** メソッドは、3 つのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="45acb-109">The **Respond** method accepts three parameters.</span></span> 

<span data-ttu-id="45acb-110">*Response* パラメーターは、応答が受諾、辞退、仮の予定のいずれであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="45acb-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="45acb-111">fNoUI と fAdditionalTextDialog は **bool** 値のパラメーターで、それぞれ、応答を送信するかどうか、ユーザーが応答を編集できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="45acb-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="45acb-112">次のコード例の AutoAcceptMeetingRequests では、すべての **MeetingItem** オブジェクトを列挙して、関連する **AppointmentItem** を取得します。</span><span class="sxs-lookup"><span data-stu-id="45acb-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="45acb-113">その後、AutoAcceptMeetingRequests では、*fNoUI* パラメーターを指定した **Respond** メソッドを使用します。このパラメーターは、会議出席依頼を受諾する応答を自動的に送信するように指示するために **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="45acb-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="45acb-114">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="45acb-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="45acb-115">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45acb-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="45acb-116">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="45acb-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="45acb-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="45acb-117">See also</span></span>

- [<span data-ttu-id="45acb-118">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="45acb-118">Meeting requests</span></span>](meeting-requests.md)

