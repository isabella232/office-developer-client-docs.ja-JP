---
title: 予定アイテムのリマインダーを作成する
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405974"
---
# <a name="create-a-reminder-for-an-appointment-item"></a><span data-ttu-id="9d30d-102">予定アイテムのリマインダーを作成する</span><span class="sxs-lookup"><span data-stu-id="9d30d-102">Create a reminder for an appointment item</span></span>

<span data-ttu-id="9d30d-103">この例では、[ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) プロパティを使用して予定アイテムのリマインダーを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-103">This example shows how to use the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property to create a reminder for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="9d30d-104">例</span><span class="sxs-lookup"><span data-stu-id="9d30d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9d30d-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="9d30d-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="9d30d-p101">Outlook では、[AppointmentItem](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) オブジェクトの [ReminderSet](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) プロパティを使用して、予定に事前通知を設定できます。このプロパティは、予定に対して事前通知が作成されているかどうかを示します。 ReminderSet プロパティを true に設定すると通知が作成され、 false に設定すると通知が削除されます。</span><span class="sxs-lookup"><span data-stu-id="9d30d-p101">Outlook provides a way to set a reminder for an appointment by using the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object. This property indicates whether a reminder has been created for the appointment. Setting the ReminderSet property to true creates a reminder, and setting it to false removes the reminder.</span></span>

<span data-ttu-id="9d30d-109">次のコード例の ReminderExample では、California 州の Napa で開催されるワイン試飲会のプライベートな予定に対するリマインダーを作成して、その予定の開始 2 時間前に通知されるようにリマインダーを設定します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-109">In the following code example,   creates a reminder on a private appointment for wine tasting in Napa, California, and sets the reminder to occur two hours before the appointment starts.</span></span> <span data-ttu-id="9d30d-110">ReminderExample では、まず、Outlook **AppointmentItem** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-110">First,   creates an Outlook AppointmentItem object.</span></span> <span data-ttu-id="9d30d-111">その後、アイテムの [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) プロパティを [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)) に設定します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-111">It then sets the [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) property for the item to [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)) .</span></span> <span data-ttu-id="9d30d-112">これにより、予定がプライベートな予定であることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-112">This indicates that the appointment is a private appointment.</span></span> <span data-ttu-id="9d30d-113">その他の予定のプロパティ ([Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) と [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) の時刻など) を設定した後で、ReminderExample では [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) プロパティを設定して、予定の開始何分前にリマインダーが表示ようにするかを指示します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-113">After setting other properties of the appointment, such as Start and End times,   sets the ReminderMinutesBeforeStart property to indicate the number of minutes that the reminder will appear before the start of the appointment.</span></span> <span data-ttu-id="9d30d-114">この例では、ReminderMinutesBeforeStart が 120 分 (2 時間) に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9d30d-114">In this case, ReminderMinutesBeforeStart is set to 120 minutes (two hours).</span></span>

<span data-ttu-id="9d30d-115">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d30d-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="9d30d-116">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d30d-116">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="9d30d-117">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9d30d-117">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="9d30d-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d30d-118">See also</span></span>

- [<span data-ttu-id="9d30d-119">予定</span><span class="sxs-lookup"><span data-stu-id="9d30d-119">Appointments</span></span>](appointments.md)

