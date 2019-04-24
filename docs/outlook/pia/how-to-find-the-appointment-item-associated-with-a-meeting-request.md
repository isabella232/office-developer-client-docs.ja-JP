---
title: 会議出席依頼に関連付けられている予定アイテムを検索する
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43bc64dbbed14dae2e185ea89d15b6061858de42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320301"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a><span data-ttu-id="a432a-102">会議出席依頼に関連付けられている予定アイテムを検索する</span><span class="sxs-lookup"><span data-stu-id="a432a-102">Find the appointment item associated with a meeting request</span></span>

<span data-ttu-id="a432a-103">この例では、[GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) メソッドを使用して会議出席依頼に関連する予定を検索する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a432a-103">This example shows how to use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to find the appointment that is associated with a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="a432a-104">例</span><span class="sxs-lookup"><span data-stu-id="a432a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a432a-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="a432a-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a432a-106">[MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) オブジェクトは、予定ではなく、受信者の予定表に予定を追加する要求を含むメッセージを表しています。</span><span class="sxs-lookup"><span data-stu-id="a432a-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object does not represent an appointment, but a message that contains a request to add an appointment to the recipient’s calendar.</span></span> <span data-ttu-id="a432a-107">次のコード例の MeetingRequestExample では、ユーザーの受信トレイから取得した各 **MeetingItem** に対して **MeetingItem** オブジェクトの [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a432a-107">In the following code example, MeetingRequestExample uses the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method of the **MeetingItem** object on each **MeetingItem** retrieved from the user’s Inbox.</span></span> <span data-ttu-id="a432a-108">その後、返された [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを使用して、予定の件名を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="a432a-108">The returned [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is then used to write the subject of the appointment to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="a432a-109">ユーザーの予定表に予定が追加されないように、**GetAssociatedAppointment** 引数を **false** に設定していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a432a-109">Note that **GetAssociatedAppointment** argument is set to **false** so that the appointment is not added to the user’s calendar.</span></span>

<span data-ttu-id="a432a-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a432a-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a432a-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a432a-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a432a-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a432a-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a432a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="a432a-113">See also</span></span>

- [<span data-ttu-id="a432a-114">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="a432a-114">Meeting requests</span></span>](meeting-requests.md)

