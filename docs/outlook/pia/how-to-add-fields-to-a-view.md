---
title: ビューにフィールドを追加する
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4b850bf87be4024152ee808624ad93836b904897
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359697"
---
# <a name="add-fields-to-a-view"></a><span data-ttu-id="134e0-102">ビューにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="134e0-102">Add fields to a view</span></span>

<span data-ttu-id="134e0-103">この例では、[ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) コレクションの [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) メソッドでビューにフィールドを追加してビューをカスタマイズする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="134e0-103">This example shows how to customize a view by using the [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) method of the [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) collection to add fields to a view.</span></span>

## <a name="example"></a><span data-ttu-id="134e0-104">例</span><span class="sxs-lookup"><span data-stu-id="134e0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="134e0-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="134e0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="134e0-106">**CardView** オブジェクトと [TableView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) オブジェクトについては、 [ViewFields](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) コレクションにプロパティを追加することで、Outlook のどのアイテム プロパティをビューに表示するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="134e0-106">You can specify which Outlook item properties are displayed in a view by adding one or more properties to the **ViewFields** collection for only the [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) and [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) objects.</span></span> <span data-ttu-id="134e0-107">その他の派生 **View** オブジェクト ([BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\))、[CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\))、[IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\))、[TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) オブジェクトなど) に対しては、ビューにどの Outlook アイテムを表示するかを決定する別のメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="134e0-107">For other derived **View** objects such as [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)), and [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) objects, use other methods of determining which Outlook item properties are displayed within the view.</span></span> <span data-ttu-id="134e0-108">たとえば、**BusinessCardView** オブジェクトで表示するフィールドは、表示する各 Outlook アイテムに関連付けられた電子名刺 (EBC) のレイアウトによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="134e0-108">For example, the fields displayed for the **BusinessCardView** object are determined by the electronic business card (EBC) layout associated with each displayed Outlook item.</span></span>

<span data-ttu-id="134e0-p102">ビューの **ViewFields** コレクションを取得するには、関連する **View** オブジェクト (たとえば、 **CardView** オブジェクトや **TableView** オブジェクト) の **ViewFields** プロパティを使用します。 **ViewFields** コレクションの **Add** メソッドを使用して、ビューに表示する Outlook のアイテム プロパティを表す [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) オブジェクトを作成します。 **ViewField** オブジェクトは、ビューに表示する Outlook のアイテム プロパティを表すだけでなく、そのプロパティをどのような値として表示するかも記述します。ビューの個々の列のプロパティの表示方法は、 [ViewField](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) オブジェクトの **ColumnFormat** プロパティで変更できます。</span><span class="sxs-lookup"><span data-stu-id="134e0-p102">To get the **ViewFields** collection for a view, use the **ViewFields** property of the associated **View** object (for example, the **CardView** or **TableView** objects). The **Add** method of the **ViewFields** collection is used to create a [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) object that represents the Outlook item property to be displayed in the view. A **ViewField** object not only identifies an Outlook item property to display within the view, but it also describes how the values for that property should be displayed. You can change how individual column properties are displayed in a view by modifying the [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) property of the **ViewField** object.</span></span>

<span data-ttu-id="134e0-p103">次のコード例の ModifyMeetingRequestsView は、ユーザーの受信トレイから "Meeting Requests" (会議出席依頼) ビューと区分されるすべてのビューを表す **TableView** オブジェクトを取得します。次に、**Add** メソッドを使用して、"Start" フィールドと "End" フィールドを、**TableView** オブジェクトに対応する **ViewFields** オブジェクトに追加します。さらに、"From" フィールドのラベルを "Organized By" (開催者) に変更します。その後、ModifyMeetingRequestsView は、変更された **TableView** オブジェクトを保存します。</span><span class="sxs-lookup"><span data-stu-id="134e0-p103">In the following code example, ModifyMeetingRequestsView gets the **TableView** object that represents all the views from the user’s Inbox that are “Meeting Requests” views. The example then uses the **Add** method to add the “Start” and “End” fields to the **ViewFields** object that corresponds to the **TableView** object. It also changes the label for the “From” field to “Organized By”. ModifyMeetingRequestsView then saves the modified **TableView** object.</span></span>

<span data-ttu-id="134e0-117">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="134e0-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="134e0-118">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="134e0-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="134e0-119">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="134e0-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="134e0-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="134e0-120">See also</span></span>

- [<span data-ttu-id="134e0-121">ビュー</span><span class="sxs-lookup"><span data-stu-id="134e0-121">Views</span></span>](views.md)

