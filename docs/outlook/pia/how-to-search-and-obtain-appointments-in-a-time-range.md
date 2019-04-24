---
title: 時間範囲内の予定を検索、取得する
TOCTitle: Search and obtain appointments in a time range
ms:assetid: ce5205ad-6967-4f21-8a9d-503b731dbd40
ms:mtpsurl: https://msdn.microsoft.com/library/Gg619398(v=office.15)
ms:contentKeyID: 55119927
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9088da5f2deb4b3d4ccb1c2bc5409e0ff280ed24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316092"
---
# <a name="search-and-obtain-appointments-in-a-time-range"></a><span data-ttu-id="fa9cb-102">時間範囲内の予定を検索、取得する</span><span class="sxs-lookup"><span data-stu-id="fa9cb-102">Search and obtain appointments in a time range</span></span>

<span data-ttu-id="fa9cb-103">この例では、既定の Microsoft Outlook の予定表にある特定の時間範囲の予定を返します。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-103">This example returns appointments in a specific time range in the default Microsoft Outlook calendar.</span></span>

## <a name="example"></a><span data-ttu-id="fa9cb-104">例</span><span class="sxs-lookup"><span data-stu-id="fa9cb-104">Example</span></span>

<span data-ttu-id="fa9cb-p101">このコード例には、DemoAppointmentsInRange と GetAppointmentsInRange の2 つのメソッドが含まれています。DemoAppointmentsInRange は、現在サインインしている Outlook のプロファイルの既定のカレンダーを取得し、今日の 12:00 AM を起点に5 日間の日付の範囲を設定し、GetAppointmentsInRange を呼び出して、その時間の範囲に入る予定を返し、返された予定それぞれの件名と開始時刻を表示します。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-p101">This code example contains two methods: DemoAppointmentsInRange and GetAppointmentsInRange. DemoAppointmentsInRange obtains the default calendar for the current signed-in Outlook profile, sets a date range of 5 days from 12:00 A.M. today, calls GetAppointmentsInRange to obtain appointments that fall in that time range, and displays the subject and start time of each of the returned appointments.</span></span>

<span data-ttu-id="fa9cb-108">GetAppointmentsInRange は、Outlook フォルダーと、時間の範囲の開始と終了の **DateTime** 値を入力パラメーターとして受け入れます。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-108">GetAppointmentsInRange accepts an Outlook folder, and the start and end **DateTime** values of the time range as input parameters.</span></span> <span data-ttu-id="fa9cb-109">このメソッドは、 [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) メソッドと、指定した時間範囲内に開始、終了する予定を返す Jet 形式の文字列フィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-109">This method uses the [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method and a string filter in Jet format that returns appointments that start and end within the specified time range.</span></span> <span data-ttu-id="fa9cb-110">\[Start\] と \[End\] を予定の開始時刻と終了時刻、startTime と endTime を指定した時間範囲の開始と終了時刻と仮定して、GetAppointmentsInRange では `[Start]>=startTime`、および `[End]<=endTime` の予定を見つけるフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-110">Assuming \[Start\] and \[End\] are the start time and end time of an appointment, and startTime and endTime are the beginning and end time of the specified time range, GetAppointmentsInRange sets up a filter  that looks for appointments with `[Start]>=startTime`, and `[End]<=endTime`.</span></span> <span data-ttu-id="fa9cb-111">次のコードは、C\# での Jet フィルターを示しています。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-111">The following code shows the Jet filter in C\#.</span></span>

```csharp
string filter = "[Start] >= '"
    + startTime.ToString("g")
    + "' AND [End] <= '"
    + endTime.ToString("g") + "'";
```

<span data-ttu-id="fa9cb-112">**Items.Restrict** メソッドを呼び出して予定を検索する前に、指定した時間範囲内で発生する定期的な予定を含めるために、GetAppointmentsInRange は他に次の 2 つの処理を行います。 </span><span class="sxs-lookup"><span data-stu-id="fa9cb-112">Before calling the **Items.Restrict** method to search for appointments, GetAppointmentsInRange does two other things to include recurring appointments that occur in the specified time range:</span></span>

- <span data-ttu-id="fa9cb-113">[Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) コレクションの [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-113">Sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection.</span></span>

- <span data-ttu-id="fa9cb-114">[Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) プロパティ別に、指定された予定表フォルダーの予定アイテムを並べ替える。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-114">Sorts the appointment items in the given calendar folder by the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span>

<span data-ttu-id="fa9cb-115">一方、指定した時間範囲にその一部または全体が重なる予定を検索したい場合は、別のフィルターを指定して、返したい予定の種類を追加します (図 1 を参照)。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-115">Alternatively, if you are also interested in appointments that overlap partially or entirely with the specified time range, you would specify a different filter to return additional types of appointments (as shown in Figure 1):</span></span>

- <span data-ttu-id="fa9cb-116">指定した時間の範囲内に開始して終了する予定 (たとえば、予定 A):</span><span class="sxs-lookup"><span data-stu-id="fa9cb-116">Appointments that start and end within the specified time range (for example, appointment A):</span></span><br/><br/>`[Start]>=startTime and [End]<=endTime`

- <span data-ttu-id="fa9cb-117">指定した時間の範囲よりも前に開始し、指定した時間の範囲内に終了する予定 (たとえば、予定 B):</span><span class="sxs-lookup"><span data-stu-id="fa9cb-117">Appointments that start before the specified time range but end within the time range (for example, appointment B):</span></span><br/><br/>`[Start]<startTime and [End]<=endTime`

- <span data-ttu-id="fa9cb-118">指定した時間の範囲内に開始し、指定した時間の範囲よりも後に終了する予定 (たとえば、予定 C):</span><span class="sxs-lookup"><span data-stu-id="fa9cb-118">Appointments that start within the specified time range but end after the time range (for example, appointment C):</span></span><br/><br/>`[Start]>=startTime and [End]>endTime`

- <span data-ttu-id="fa9cb-119">指定した時間の範囲よりも前に開始し、指定した時間の範囲よりも後に終了する予定 (たとえば、予定 D):</span><span class="sxs-lookup"><span data-stu-id="fa9cb-119">Appointments that start before the specified time range and end after the time range (for example, appointment D):</span></span><br/><br/>`[Start]<startTime and [End]>endTime`

<span data-ttu-id="fa9cb-120">**図 1. 時間の範囲内で発生するか、その時間の範囲に重なる予定の種類**</span><span class="sxs-lookup"><span data-stu-id="fa9cb-120">**Figure 1. Types of appointments that occur within a time range, or overlap with that time range**</span></span>

![時間の範囲内で発生するか、その時間の範囲に重なる予定の種類](media/pia-appointment-starttime-endtime.gif)
 

<span data-ttu-id="fa9cb-122">どのような時間の範囲も `startTime<=endTime` になるため、`[Start]<=endTime` および `[End]>=startTime` のフィルターによって、その時間の範囲に含まれる上記の種類の予定が取得されます。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-122">Because in any time range `startTime<=endTime`, a filter with `[Start]<=endTime` and `[End]>=startTime` would capture the preceding types of appointments in that time range.</span></span>

<span data-ttu-id="fa9cb-123">C\# では、Jet フィルターを次のように表現できます。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-123">In C\#, you can express the Jet filter as follows.</span></span>

```csharp
string filter = "[Start] <= '"
    + endTime.ToString("g")
    + "' AND [End] >= '"
    + startTime.ToString("g") + "'";
```

<span data-ttu-id="fa9cb-124">次のコードは、完全な例を示しています。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-124">The following code shows the complete example.</span></span> <span data-ttu-id="fa9cb-125">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-125">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fa9cb-126">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-126">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fa9cb-127">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fa9cb-127">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoAppointmentsInRange()
{
    Outlook.Folder calFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    DateTime start = DateTime.Now;
    DateTime end = start.AddDays(5);
    Outlook.Items rangeAppts = GetAppointmentsInRange(calFolder, start, end);
    if (rangeAppts != null)
    {
        foreach (Outlook.AppointmentItem appt in rangeAppts)
        {
            Debug.WriteLine("Subject: " + appt.Subject 
                + " Start: " + appt.Start.ToString("g"));
        }
    }
}

/// <summary>
/// Get recurring appointments in date range.
/// </summary>
/// <param name="folder"></param>
/// <param name="startTime"></param>
/// <param name="endTime"></param>
/// <returns>Outlook.Items</returns>
private Outlook.Items GetAppointmentsInRange(
    Outlook.Folder folder, DateTime startTime, DateTime endTime)
{
    string filter = "[Start] >= '"
        + startTime.ToString("g")
        + "' AND [End] <= '"
        + endTime.ToString("g") + "'";
    Debug.WriteLine(filter);
    try
    {
        Outlook.Items calItems = folder.Items;
        calItems.IncludeRecurrences = true;
        calItems.Sort("[Start]", Type.Missing);
        Outlook.Items restrictItems = calItems.Restrict(filter);
        if (restrictItems.Count > 0)
        {
            return restrictItems;
        }
        else
        {
            return null;
        }
    }
    catch { return null; }
}
```

## <a name="see-also"></a><span data-ttu-id="fa9cb-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa9cb-128">See also</span></span>

- [<span data-ttu-id="fa9cb-129">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="fa9cb-129">Search and filter</span></span>](search-and-filter.md)

