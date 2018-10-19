---
title: 既定の定期的なパターンを使用して、定期的な予定を作成する
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: be6c024012c02d31af7ce37af6010ba6b40419ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406709"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a><span data-ttu-id="1e6c4-102">既定の定期的なパターンを使用して、定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="1e6c4-102">Creates a recurring appointment by using the default recurrence pattern.</span></span>

<span data-ttu-id="1e6c4-103">この例では、既定の定期的なパターンを使用して定期的な予定を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-103">This example shows how to create a recurring appointment by using the default recurrence pattern.</span></span>

## <a name="example"></a><span data-ttu-id="1e6c4-104">例</span><span class="sxs-lookup"><span data-stu-id="1e6c4-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1e6c4-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="1e6c4-106">Outlook で予定を作成するときには、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-106">When you create an appointment in Outlook, you are creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="1e6c4-107">予定は、AppointmentItem の [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) プロパティを true に設定することで定期的な予定になります。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-107">Your appointment is a recurring appointment if the [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) property of the AppointmentItem is set to true.</span></span> <span data-ttu-id="1e6c4-108">IsRecurring は、直接設定することができません。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-108">IsRecurring cannot be set directly.</span></span> 

<span data-ttu-id="1e6c4-109">ただし、[RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトを使用することで、定期的な予定を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-109">However, you can create a recurring appointment by using the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="1e6c4-110">プログラムで定期的な予定を作成するには、**AppointmentItem** オブジェクトを作成し、**AppointmentItem** オブジェクトの [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) メソッドを呼び出してから、**AppointmentItem** オブジェクトを保存します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-110">To create a recurring appointment programmatically, create an **AppointmentItem** object, call the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method of the **AppointmentItem** object, and then save the **AppointmentItem** object.</span></span> <span data-ttu-id="1e6c4-111">これにより、既定の定期的なパターンを使用する予定が作成されます。このパターンでは、予約は毎週予定が作成された曜日に発生し、終了日はありません。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-111">This creates an appointment that uses the default recurrence pattern, which occurs weekly on the day of the week for which the appointment was created, and has no end date.</span></span> <span data-ttu-id="1e6c4-112">RecurrencePattern オブジェクトを使用すると、指定した間隔 (日次、週次、月次、年次) で繰り返される定期的な予定を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-112">The RecurrencePattern object allows you to create recurring appointments at specified intervals—daily, weekly, monthly, or yearly.</span></span> <span data-ttu-id="1e6c4-113">RecurrencePattern に間隔を指定しない場合、Outlook では既定の定期的なパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-113">If you do not specify intervals for the RecurrencePattern object, Outlook will use the default recurrence pattern.</span></span>

<span data-ttu-id="1e6c4-114">定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-114">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="1e6c4-115">この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-115">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="1e6c4-116">Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-116">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="1e6c4-117">C\# では、そのオブジェクトのメモリを明示的に解放します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-117">In C#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="1e6c4-p104">参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="1e6c4-120">次の例の CreateRecurringAppointment では、**AppointmentItem** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-120">In the following code example,   creates an AppointmentItem object and sets some of its properties.</span></span> <span data-ttu-id="1e6c4-121">その後で、GetRecurrencePattern を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-121">It then calls GetRecurrencePattern.</span></span> <span data-ttu-id="1e6c4-122">GetRecurrencePattern から RecurrencePattern オブジェクトが返され、AppointmentItem オブジェクトが保存されます。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-122">GetRecurrencePattern returns a RecurrencePattern object, and the AppointmentItem is saved.</span></span> <span data-ttu-id="1e6c4-123">これにより、既定の定期的なパターンを使用する定期的な予定が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-123">This creates a recurring appointment that uses the default recurrence pattern.</span></span>

<span data-ttu-id="1e6c4-124">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-124">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="1e6c4-125">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-125">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="1e6c4-126">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-126">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="1e6c4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e6c4-127">See also</span></span>

- [<span data-ttu-id="1e6c4-128">予定</span><span class="sxs-lookup"><span data-stu-id="1e6c4-128">Appointments</span></span>](appointments.md)

