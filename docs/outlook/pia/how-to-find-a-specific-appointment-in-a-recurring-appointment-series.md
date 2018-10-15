---
title: 定期的な一連の予定から特定の予定を検索する
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ab245fc0ff9b60862cebe57fbb2d996735442b89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405869"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="3cfe8-102">定期的な一連の予定から特定の予定を検索する</span><span class="sxs-lookup"><span data-stu-id="3cfe8-102">Find a specific appointment in a recurring appointment series</span></span>

<span data-ttu-id="3cfe8-103">この例では、一連の定期的な予定のうちの特定の予定を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-103">This example shows how to return an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a specific appointment in a recurring appointment series.</span></span>

## <a name="example"></a><span data-ttu-id="3cfe8-104">例</span><span class="sxs-lookup"><span data-stu-id="3cfe8-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3cfe8-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="3cfe8-106">特定の日付および時刻に発生する定期的な予定のインスタンスを見つけるには、[RecurrencePattern](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) オブジェクトの [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) メソッドを使用して、 **AppointmentItem** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-106">To find an instance of a recurring appointment that occurs at a specified date and time, use the [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) method of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to return an **AppointmentItem** object.</span></span>

<span data-ttu-id="3cfe8-107">定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-107">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="3cfe8-108">この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-108">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="3cfe8-109">Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-109">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="3cfe8-110">C\# では、そのオブジェクトのメモリを明示的に解放します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-110">In C#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="3cfe8-p102">参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-p102">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="3cfe8-113">次のコード例の CheckOccurrenceExample では、「[週単位パターンの定期的な予定を作成する](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)」で作成した定期的な予定を使用します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-113">In the following code example, CheckOccurrenceExample uses the recurring appointment that was created in the code example in [Create a Recurring Appointment That Has a Weekly Pattern](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span></span> <span data-ttu-id="3cfe8-114">GetOccurrence メソッドを呼び出して、定期的な予定の開始日と時刻が指定されているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-114">It then calls the GetOccurrence method to determine whether the recurring appointment starts on the specified date and time.</span></span> <span data-ttu-id="3cfe8-115">定期的な予定のインスタンスの開始日と時刻が指定の情報と一致しない場合でもプロシージャが続行されるように、この例では try…catch ブロックを使用しています。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-115">To ensure that the procedure will continue even if the provided information does not match the start date and time of an instance of the recurring appointment, the example uses a try…catch block.</span></span> <span data-ttu-id="3cfe8-116">CheckOccurrenceExample では、一連の定期的な予定に含まれる予定ごとに GetOccurrence メソッドを呼び出してから、singleAppt 変数をテストして、その変数が null 参照に設定されているかどうかを調べます。この null 参照は、メソッドが失敗して **AppointmentItem** オブジェクトが返されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-116">After calling the GetOccurrence method on every appointment in the recurring appointment series, CheckOccurrenceExample tests the singleAppt variable to determine whether it is set to a null reference, indicating that the method failed and did not return an **AppointmentItem** object.</span></span>

<span data-ttu-id="3cfe8-117">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="3cfe8-118">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-118">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="3cfe8-119">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3cfe8-119">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
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
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3cfe8-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="3cfe8-120">See also</span></span>

- [<span data-ttu-id="3cfe8-121">予定</span><span class="sxs-lookup"><span data-stu-id="3cfe8-121">Appointments</span></span>](appointments.md)

