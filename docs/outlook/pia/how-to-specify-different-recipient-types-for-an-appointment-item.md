---
title: 予定アイテムに異なる受信者の種類を指定する
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: beb29c46d590938d1650dac0c862dd5f898333fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335414"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a><span data-ttu-id="08731-102">予定アイテムに異なる受信者の種類を指定する</span><span class="sxs-lookup"><span data-stu-id="08731-102">Specify different recipient types for an appointment item</span></span>

<span data-ttu-id="08731-103">この例では、[OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) 列挙値を使用して予定アイテムに異なる受信者の種類を指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="08731-103">This example shows how to use the [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) enumeration to specify different recipient types for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="08731-104">例</span><span class="sxs-lookup"><span data-stu-id="08731-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="08731-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="08731-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="08731-106">会議出席依頼を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトに受信者を追加するには、 OlMeetingRecipientType 列挙値を使用して、メッセージの受信者が必須または任意の出席者か、それともリソース (部屋や機器など) かを指定します。</span><span class="sxs-lookup"><span data-stu-id="08731-106">To add recipients to an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request, use the OlMeetingRecipientType enumeration to specify whether the recipient of the message is a required or optional attendee, or a resource (such as a room or equipment).</span></span>

<span data-ttu-id="08731-107">次のコード例の SetRecipientTypeForAppt では、**AppointmentItem** オブジェクトを作成し、そのオブジェクトにプロパティを設定して、必須および任意の出席者を追加します。</span><span class="sxs-lookup"><span data-stu-id="08731-107">In the following code example, SetRecipientTypeForAppt creates an **AppointmentItem** object, sets properties for that object, and adds required and optional attendees.</span></span> <span data-ttu-id="08731-108">また、会議用の会議室も追加します。</span><span class="sxs-lookup"><span data-stu-id="08731-108">It also adds a conference room for the meeting.</span></span> <span data-ttu-id="08731-109">[MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) プロパティを [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)) に設定し、予定が会議出席依頼であることを示します。</span><span class="sxs-lookup"><span data-stu-id="08731-109">Note that the [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) property is set to [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), indicating that the appointment is a meeting request.</span></span>

<span data-ttu-id="08731-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="08731-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="08731-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08731-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="08731-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="08731-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
        appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="08731-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="08731-113">See also</span></span>

- [<span data-ttu-id="08731-114">予定</span><span class="sxs-lookup"><span data-stu-id="08731-114">Appointments</span></span>](appointments.md)

