---
title: 定期的な一連の予定に例外的な予定を作成する
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356435"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="e73a0-102">定期的な一連の予定に例外的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="e73a0-102">Create an exception appointment in a recurring appointment series</span></span>

<span data-ttu-id="e73a0-103">この例では、[Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトを使用して、予定に対する標準の定期的なパターンの例外を作成します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-103">This example uses an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object to create an exception to a standard recurrence pattern for an appointment.</span></span>

## <a name="example"></a><span data-ttu-id="e73a0-104">例</span><span class="sxs-lookup"><span data-stu-id="e73a0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e73a0-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="e73a0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e73a0-106">定期的な予定の 1 つの予定のインスタンスを削除または変更すると、Outlook によって [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e73a0-106">Once you delete or change one appointment instance of a recurring appointment, Outlook creates an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object.</span></span> <span data-ttu-id="e73a0-107">Exception オブジェクトを使用すると、標準の定期的なパターンに例外を作成できます。</span><span class="sxs-lookup"><span data-stu-id="e73a0-107">The Exception object allows you to create an exception to a standard recurrence pattern.</span></span> <span data-ttu-id="e73a0-108">オブジェクトのプロパティには、予定のインスタンスに加えられた変更が格納されています。</span><span class="sxs-lookup"><span data-stu-id="e73a0-108">The object’s properties contain the changes that were made to the appointment instance.</span></span> <span data-ttu-id="e73a0-109">[Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) コレクションには、定期的な予定の Exception オブジェクトがすべて収容されています。さらに、このコレクションは、予定の [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="e73a0-109">The [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) collection contains all of the Exception objects for a recurring appointment, and is associated with the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span>

<span data-ttu-id="e73a0-110">定期的な予定の元の定期的なパターンに対する例外を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを取得するには、Exception の [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-110">To get the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents the exception to the original recurrence pattern of the recurring appointment, use the [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) property of the Exception.</span></span> <span data-ttu-id="e73a0-111">返された AppointmentItem のメソッドとプロパティを使用すると、予定の例外のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e73a0-111">By using the methods and properties of the returned AppointmentItem, you can set the properties of the appointment exception.</span></span>

<span data-ttu-id="e73a0-112">定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e73a0-112">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="e73a0-113">この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。</span><span class="sxs-lookup"><span data-stu-id="e73a0-113">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="e73a0-114">Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-114">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="e73a0-115">C\# では、そのオブジェクトのメモリを明示的に解放します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-115">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="e73a0-p104">参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して、別のアドインまたは Outlook が保持するアクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e73a0-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference, held by another add-in or Outlook, to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="e73a0-118">次のコード例の CreateExceptionExample では、定期的な予定の件名を変更します。この予定は、トピック「[定期的な一連の予定から特定の予定を検索する](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)」で作成したものです。その後、結果の Exception オブジェクトの AppointmentItem プロパティを使用して、予定の例外に対応する AppointmentItem を取得します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-118">In the following code example, CreateExceptionExample changes the subject of the recurring appointment that was created in the topic [Find a Specific Appointment in a Recurring Appointment Series](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), and then uses the AppointmentItem property of the resulting Exception object to retrieve the AppointmentItem that corresponds to the appointment exception.</span></span> <span data-ttu-id="e73a0-119">さらに、CreateExceptionExample では、予定の例外の開始時刻と終了時刻を変更します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-119">CreateExceptionExample then changes the start and end times of the appointment exception.</span></span>

<span data-ttu-id="e73a0-120">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e73a0-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e73a0-121">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e73a0-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e73a0-122">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e73a0-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e73a0-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e73a0-123">See also</span></span>

- [<span data-ttu-id="e73a0-124">予定</span><span class="sxs-lookup"><span data-stu-id="e73a0-124">Appointments</span></span>](appointments.md)

