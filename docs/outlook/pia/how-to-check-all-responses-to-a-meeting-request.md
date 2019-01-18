---
title: 会議出席依頼へのすべての返信を調べる
TOCTitle: Check all responses to a meeting request
ms:assetid: ebe10e5a-7f04-447a-bfc1-aa8a726cb0b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184650(v=office.15)
ms:contentKeyID: 55119881
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89f3aa7037659bb29346bb70338d535cbbc200b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709244"
---
# <a name="check-all-responses-to-a-meeting-request"></a><span data-ttu-id="137ef-102">会議出席依頼へのすべての返信を調べる</span><span class="sxs-lookup"><span data-stu-id="137ef-102">Check all responses to a meeting request</span></span>

<span data-ttu-id="137ef-103">この例では、会議出席依頼に対する各受信者の返信の状態を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="137ef-103">This example shows how to check the status of each recipient’s response to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="137ef-104">例</span><span class="sxs-lookup"><span data-stu-id="137ef-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="137ef-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="137ef-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="137ef-106">次のコード例の CheckAttendeeStatus では、会議出席依頼を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションを列挙し、各 [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトの [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) プロパティを調べます。</span><span class="sxs-lookup"><span data-stu-id="137ef-106">In the following code example, CheckAttendeeStatus enumerates the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request and examines the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object.</span></span> <span data-ttu-id="137ef-107">各 **Recipient** オブジェクトは、会議出席依頼の受信者を表します。</span><span class="sxs-lookup"><span data-stu-id="137ef-107">Each **Recipient** object represents a recipient of the meeting request.</span></span> <span data-ttu-id="137ef-108">**MeetingResponseStatus** プロパティの値は、次の [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) 列挙値のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="137ef-108">The value of the **MeetingResponseStatus** property can be one of the following [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) enumeration values:</span></span>

- <span data-ttu-id="137ef-109">[olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="137ef-109">[olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="137ef-110">[olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="137ef-110">[olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="137ef-111">[olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="137ef-111">[olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="137ef-112">[olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="137ef-112">[olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="137ef-113">[olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="137ef-113">[olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="137ef-114">[olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="137ef-114">[olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>

<span data-ttu-id="137ef-115">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="137ef-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="137ef-116">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="137ef-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="137ef-117">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="137ef-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CheckAttendeeStatus()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find("[Subject]='Sales Strategy FY2007'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            switch (recip.MeetingResponseStatus)
            {
                case Outlook.OlResponseStatus.olResponseAccepted:
                    Debug.WriteLine("Accepted: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseTentative:
                    Debug.WriteLine("Tentative: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseDeclined:
                    Debug.WriteLine("Declined: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseOrganized:
                    Debug.WriteLine("Organizer: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNone:
                    Debug.WriteLine("None: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNotResponded:
                    Debug.WriteLine("Not responded: " + recip.Name);
                    break;
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="137ef-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="137ef-118">See also</span></span>

- [<span data-ttu-id="137ef-119">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="137ef-119">Meeting requests</span></span>](meeting-requests.md)

