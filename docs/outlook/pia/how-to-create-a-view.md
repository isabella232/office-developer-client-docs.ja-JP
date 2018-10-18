---
title: ビューを作成する
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e9a68fc6220e1439e517b3d4e7e2ecb30b919ee0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406030"
---
# <a name="create-a-view"></a><span data-ttu-id="599bb-102">ビューを作成する</span><span class="sxs-lookup"><span data-stu-id="599bb-102">Create a map view programmatically</span></span>

<span data-ttu-id="599bb-103">この例では、[Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) コレクションの [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) メソッドを使用して [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトのビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="599bb-103">This example shows how to use the [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) method of the [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) collection to create a view for a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="599bb-104">例</span><span class="sxs-lookup"><span data-stu-id="599bb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="599bb-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="599bb-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="599bb-p101">Outlook エクスプローラー ウィンドウのビュー ウィンドウ内で種類の異なるデータの並べ替え、グループ化、および表示ができるカスタマイズ可能なビューを作成できます。組み込みビューをプログラムによってカスタマイズすることもできます。次の表は、Outlook のビューを表現するオブジェクトの一覧です。</span><span class="sxs-lookup"><span data-stu-id="599bb-p101">You can create customizable views that allow you to sort, group, and view data of all different types within the View Pane of the Outlook explorer window. You can also customize built-in views programmatically. The following table lists objects that represent Outlook views.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="599bb-109">オブジェクト名</span><span class="sxs-lookup"><span data-stu-id="599bb-109">Object Name</span></span></p></th>
<th><p><span data-ttu-id="599bb-110">説明</span><span class="sxs-lookup"><span data-stu-id="599bb-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="599bb-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span><span class="sxs-lookup"><span data-stu-id="599bb-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="599bb-112">データは一連の電子名刺画像として表示されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-112">Data is viewed as a series of Electronic Business Card images.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599bb-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span><span class="sxs-lookup"><span data-stu-id="599bb-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span></span></p></td>
<td><p><span data-ttu-id="599bb-114">データが予定表の形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-114">Data is viewed in a calendar format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599bb-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span><span class="sxs-lookup"><span data-stu-id="599bb-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="599bb-116">データが一連のカードで表示されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-116">Data is viewed in a series of cards.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599bb-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span><span class="sxs-lookup"><span data-stu-id="599bb-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView Object</a></span></span></p></td>
<td><p><span data-ttu-id="599bb-118">データが Windows のフォルダー アイコンまたはエクスプローラー アイコンとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-118">Data is viewed as Windows folder icons or explorer icons.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599bb-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span><span class="sxs-lookup"><span data-stu-id="599bb-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView Object</a></span></span></p></td>
<td><p><span data-ttu-id="599bb-120">データが単純なフィールド ベースの表で表示されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-120">Data is viewed in a simple field-based table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599bb-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span><span class="sxs-lookup"><span data-stu-id="599bb-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView Object</a></span></span></p></td>
<td><p><span data-ttu-id="599bb-122">データがカスタマイズ可能な直線状のタイムラインで表示されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-122">Data is viewed in a customizable linear time line.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="599bb-123">[View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) オブジェクトを使用すると、すべてのビューに共通するプロパティとメソッドにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="599bb-123">You can access properties and methods that are common to all views by using the [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) object.</span></span> <span data-ttu-id="599bb-124">ただし、すべてのビューに共通ではない一部のプロパティにアクセスするにするには、**View** オブジェクトを、アクセスするプロパティが属する派生 **View** オブジェクトにキャストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="599bb-124">However, to access certain properties that are not common to all views, you must cast the View object to a derived view object that the property you want to access belongs to.</span></span> <span data-ttu-id="599bb-125">たとえば、**Cardview** オブジェクトの [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) プロパティにアクセスするには、**View** オブジェクトを **Cardview** オブジェクトにキャストします。</span><span class="sxs-lookup"><span data-stu-id="599bb-125">For example, to access the [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) property of the **Cardview** object, cast the **View** object to the **CardView** object.</span></span> <span data-ttu-id="599bb-126">特定の **View** オブジェクトでどの種類のビューが表示されるかを確認するには [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="599bb-126">If you want to determine which type of view is represented by a particular **View** object, use the [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) property.</span></span>

<span data-ttu-id="599bb-127">新しいビューを作成するには、 **Folder** オブジェクトに対する **Views** コレクションの **Add** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="599bb-127">To create a new view, use the **Add** method of the **Views** collection for a **Folder** object.</span></span> <span data-ttu-id="599bb-128">次に、ビューの作成時または作成後のいずれかでビューの可視性を設定します。</span><span class="sxs-lookup"><span data-stu-id="599bb-128">Then set the visibility for the view either at the time of creation, or at any time after the view is created.</span></span> <span data-ttu-id="599bb-129">ビューの可視性を作成時に設定するには、**Add** メソッドで *SaveOption* パラメーターの [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) 定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="599bb-129">To set the visibility for the view at the time of creation, specify an [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) constant in the  *SaveOption* parameter of the **Add** method.</span></span> <span data-ttu-id="599bb-130">ビューの可視性をビューの作成後の任意の時点で設定するには、 **View** オブジェクトの [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) プロパティに対して **OlViewSaveOption** 定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="599bb-130">To set the visibility at any time after the view is created, specify an **OlViewSaveOption** constant for the [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) property of the **View** object.</span></span> 

<span data-ttu-id="599bb-131">新しいビューを追加すると、 [Views](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) コレクションの **ViewAdd** イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="599bb-131">Adding a new view raises the [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) event of the **Views** collection.</span></span> <span data-ttu-id="599bb-132">ビューが作成されたら、 **View** オブジェクトを派生オブジェクトの 1 つにキャストしてから必要な変更を行うことにより、そのビューをプログラムでカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="599bb-132">Once the view is created, customize the view programmatically by casting the **View** object to one of the derived objects and then making necessary changes.</span></span> <span data-ttu-id="599bb-133">派生 **View** オブジェクトまたは **View** オブジェクトの **Save** メソッドを使用してビューへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="599bb-133">Use the Save method of the derived view object or the View object to save any changes to the view.</span></span> <span data-ttu-id="599bb-134">最後に、派生 **View** オブジェクトまたは **View** オブジェクトの **Apply** メソッドを使用してビューを現在の [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトに適用します。</span><span class="sxs-lookup"><span data-stu-id="599bb-134">Finally, use the Apply method of the derived view object or the View object to apply the view to the current Explorer object.</span></span> <span data-ttu-id="599bb-135">これにより、**Explorer** オブジェクトの [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="599bb-135">This raises the [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) event of the **Explorer** object.</span></span>

<span data-ttu-id="599bb-136">次のコード例では、**View** オブジェクトを **TableView** オブジェクトにキャストすると、CreateMeetingRequestsView が “Meeting Requests” という名前の新しいビューをユーザーの受信トレイに追加します。</span><span class="sxs-lookup"><span data-stu-id="599bb-136">In the following code example, CreateMeetingRequestsView adds a new view named “Meeting Requests” to the user’s Inbox by casting the **View** object to a **TableView** object.</span></span> <span data-ttu-id="599bb-137">次に、CreateMeetingRequestsView は、 *Name* パラメーターは “Meeting Requests”、また *ViewType* パラメーターは **olTableView** という設定で **View** オブジェクトの **Add** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="599bb-137">CreateMeetingRequestsView then calls the **Add** method of the **Views** object with the *Name* parameter set to “Meeting Requests” and the *ViewType* parameter set to **olTableView**.</span></span> <span data-ttu-id="599bb-138">**TableView** オブジェクトの [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) プロパティは、アイテムのメッセージ クラスに “IPM.Schedule” が含まれているアイテムが存在する場合に限りビューを表示させる DAV Searching and Locating (DASL) 文字列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-138">The [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) property of the **TableView** object is set to a DAV Searching and Locating (DASL) string that causes the view to display only when there are items that contain “IPM.Schedule” in the message class for the item.</span></span> <span data-ttu-id="599bb-139">新しいビューが保存され、適用されます。</span><span class="sxs-lookup"><span data-stu-id="599bb-139">The new view is then saved and applied.</span></span>

<span data-ttu-id="599bb-140">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="599bb-140">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="599bb-141">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="599bb-141">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="599bb-142">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="599bb-142">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a><span data-ttu-id="599bb-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="599bb-143">See also</span></span>

- [<span data-ttu-id="599bb-144">ビュー</span><span class="sxs-lookup"><span data-stu-id="599bb-144">Views</span></span>](views.md)

