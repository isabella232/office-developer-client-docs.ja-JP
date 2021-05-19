---
title: '[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる'
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335379"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a><span data-ttu-id="d9ac2-102">[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる</span><span class="sxs-lookup"><span data-stu-id="d9ac2-102">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>

<span data-ttu-id="d9ac2-103">この例では、**[名前の選択]** ダイアログ ボックスを使用して、予定アイテムに対する受信者を取得して割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-103">This example shows how to use the **Select Names** dialog box to obtain and assign recipients to an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="d9ac2-104">例</span><span class="sxs-lookup"><span data-stu-id="d9ac2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d9ac2-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d9ac2-p101">[ **名前の選択**] ダイアログ ボックスを表示するには、[SelectNamesDialog](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) オブジェクトの [Display()](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) メソッドを呼び出します。[ **名前の選択**] ダイアログ ボックスをユーザーに対して表示した後、ユーザーが [ **OK**] をクリックするまで、またはダイアログ ボックスを閉じるまで、コードの実行は停止します。ダイアログ ボックスに初期値として表示する受信者を設定したり、ダイアログ ボックスで選択された受信者を取得したりするには、 [SelectNamesDialog](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) オブジェクトの **Recipients** プロパティを使用します。このプロパティは、 [SelectNamesDialog](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) と関連付けられた **Recipients** コレクションを返します。 [SelectNamesDialog](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) の **Recipients** コレクションに **Recipient** オブジェクトを追加するには、コレクションの [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) メソッドを使用し、 [Recipient](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) オブジェクトの **Type** プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-p101">To display the **Select Names** dialog box, call the [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) method of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object. Once the **Select Names** dialog box is displayed to the user, code execution halts until the user clicks **OK** or closes the dialog box. To set initial recipients to display in the dialog box, or to get the recipients selected in the dialog box, use the [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) property of the **SelectNamesDialog** object. This returns a [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that is associated with the **SelectNamesDialog**. To add a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to the **Recipients** collection for the **SelectNamesDialog**, use the [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method for the collection and specify the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the **Recipient** object.</span></span>

<span data-ttu-id="d9ac2-111">次のコード例の DemoSelectNamesDialogRecipients では、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成し、いくつかのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-111">In the following code example, DemoSelectNamesDialogRecipients creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object and sets some of its properties.</span></span> <span data-ttu-id="d9ac2-112">その後、 **SelectNamesDialog** を作成し、 [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) メソッドを使用して、[ **名前の選択**] ダイアログ ボックスの会議表示モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-112">It then creates a **SelectNamesDialog** and uses the [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) method to set a meeting display mode for the **Select Names** dialog box.</span></span> <span data-ttu-id="d9ac2-113">この例では、 **Resource** 受信者セレクターに "Conf Room 36/2739" という文字列を設定します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-113">The example populates the **Resource** recipient selector with the string "Conf Room 36/2739".</span></span> <span data-ttu-id="d9ac2-114">ダイアログ ボックスをユーザーに表示した後、コードでは **SelectNamesDialog** のこのインスタンスと関連付けられている **Recipients** コレクションを列挙し、これらの受信者を作成された予定に追加します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-114">Once the dialog box is displayed to the user, the code enumerates the **Recipients** collection that is associated with this instance of **SelectNamesDialog** and adds those recipients to the appointment that was created.</span></span> <span data-ttu-id="d9ac2-115">最後に、会議出席依頼をユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-115">Finally, the example displays the meeting request to the user.</span></span>

<span data-ttu-id="d9ac2-116">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-116">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d9ac2-117">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-117">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d9ac2-118">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9ac2-118">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="d9ac2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9ac2-119">See also</span></span>

- [<span data-ttu-id="d9ac2-120">受信者</span><span class="sxs-lookup"><span data-stu-id="d9ac2-120">Recipients</span></span>](recipients.md)

