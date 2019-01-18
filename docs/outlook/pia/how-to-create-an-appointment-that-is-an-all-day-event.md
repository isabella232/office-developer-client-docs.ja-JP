---
title: 終日イベントの予定を作成する
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710826"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a><span data-ttu-id="c848f-102">終日イベントの予定を作成する</span><span class="sxs-lookup"><span data-stu-id="c848f-102">Create an appointment that is an all-day event</span></span>

<span data-ttu-id="c848f-103">この例では、[AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) プロパティを使用して終日イベントである予定を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c848f-103">This example shows how use the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property to create an appointment that is an all-day event.</span></span>

## <a name="example"></a><span data-ttu-id="c848f-104">例</span><span class="sxs-lookup"><span data-stu-id="c848f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c848f-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="c848f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="c848f-p101">イベントは、24 時間以上継続するアクティビティである点が定期的な予定とは異なります。イベントの例としては、展示会、セミナー、休暇などがあります。イベントおよび例年のイベントは、ユーザーの予定表では時間のブロックを占めるアイテムとしては表示されません。代わりに、バナーとして表示されます。バナーは、予定表の日ビューまたは週ビューの最上部に表示されます。終日の予定の場合、既定では、そのユーザーの時間は他のユーザーに対しては "予定あり" として表示されますが、イベントまたは例年のイベントの場合はユーザーの時間は "空き" として表示されます。</span><span class="sxs-lookup"><span data-stu-id="c848f-p101">An event is different from a regular appointment because it is an activity that lasts 24 hours or longer. Examples of events include trade shows, seminars, or vacations. Events and annual events do not appear as occupied blocks of time in the user’s calendar. Instead, they appear as banners. You can see the banners at the top of a calendar day or week view. For an all-day appointment, by default, the user’s time is displayed as busy when viewed by other people, but the user’s time is displayed as free for an event or annual event.</span></span>

<span data-ttu-id="c848f-112">終日イベントをプログラムで作成する場合は、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) プロパティを true に設定します。</span><span class="sxs-lookup"><span data-stu-id="c848f-112">To create an all-day event programmatically, set the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object to true.</span></span> <span data-ttu-id="c848f-113">その後で、AppointmentItem の [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) プロパティと [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c848f-113">Then set the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) properties of the AppointmentItem.</span></span> <span data-ttu-id="c848f-114">AllDayEvent プロパティを true に設定し、 Start および End プロパティを設定しないと、イベントはその日に発生し、予定として扱われ、予定表には予定あり状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c848f-114">If you set the AllDayEvent property to true and do not set the Start and End properties, the event will occur today, and it will be an appointment, showing a busy status on your calendar.</span></span> <span data-ttu-id="c848f-115">将来の日付でイベントが発生するようにする場合は、Start プロパティと End プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c848f-115">You must set the Start and End properties if you want the event to occur on a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="c848f-116">予定を終日イベントにするには、Start プロパティをイベント開始日の午前 12 時 00 分 </span><span class="sxs-lookup"><span data-stu-id="c848f-116">To make the appointment an all-day event, you must set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="c848f-117">(午前 0 時) に設定し、End プロパティをイベント終了日の翌日の午前 12 時 00 分</span><span class="sxs-lookup"><span data-stu-id="c848f-117">(midnight) on the day you want the event to begin, and set End property to 12:00 A.M.</span></span> <span data-ttu-id="c848f-118">に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c848f-118">on the day after you want the event to end.</span></span> <span data-ttu-id="c848f-119">Start または End の時刻を午前 12 時 00 分以外の日時値に設定すると、その予定は終日イベントではなく、複数日のイベントになります。</span><span class="sxs-lookup"><span data-stu-id="c848f-119">If you set the Start or End time to a date and time value other than 12:00 A.M., the appointment will become a multiday appointment instead of an all-day event.</span></span> 
>
> <span data-ttu-id="c848f-120">たとえば、期間が 1 日だけのイベントの場合は、Start プロパティをイベント開始日の午前 12 時 00 分</span><span class="sxs-lookup"><span data-stu-id="c848f-120">For example, if your event duration is only one day, set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="c848f-121">に設定し、End プロパティを次の日の午前 12 時 00 分</span><span class="sxs-lookup"><span data-stu-id="c848f-121">on the day you want the event to begin, and set the End property to 12:00 A.M.</span></span> <span data-ttu-id="c848f-122">に設定します。</span><span class="sxs-lookup"><span data-stu-id="c848f-122">on the following day.</span></span> <span data-ttu-id="c848f-123">End プロパティは、常に、開始日の翌日以降の午前 12 時 00 分</span><span class="sxs-lookup"><span data-stu-id="c848f-123">You should always set the End property to 12:00 A.M.</span></span> <span data-ttu-id="c848f-124">に設定してください。</span><span class="sxs-lookup"><span data-stu-id="c848f-124">on a date that is more than one day after the start date.</span></span>

<span data-ttu-id="c848f-p105">次のコード例の AllDayEventExample では、2007 年 6 月 11 日に開始し、2007 年 6 月 15 日に終了する終日イベントを作成しています。End プロパティが 2007 年 6 月 16 日の 12:00 A.M. に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c848f-p105">In the following code example, AllDayEventExample creates an all-day event that begins on June 11, 2007, and ends on June 15, 2007. Note that the End property for the appointment is set to 12:00 A.M. on June 16, 2007.</span></span>

<span data-ttu-id="c848f-128">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c848f-128">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c848f-129">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c848f-129">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c848f-130">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c848f-130">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="c848f-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c848f-131">See also</span></span>

- [<span data-ttu-id="c848f-132">予定</span><span class="sxs-lookup"><span data-stu-id="c848f-132">Appointments</span></span>](appointments.md)

