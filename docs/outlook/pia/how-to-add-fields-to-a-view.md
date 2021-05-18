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
# <a name="add-fields-to-a-view"></a>ビューにフィールドを追加する

この例では、[ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) コレクションの [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) メソッドでビューにフィールドを追加してビューをカスタマイズする方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


**CardView** オブジェクトと [TableView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) オブジェクトについては、 [ViewFields](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) コレクションにプロパティを追加することで、Outlook のどのアイテム プロパティをビューに表示するかを指定できます。 その他の派生 **View** オブジェクト ([BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\))、[CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\))、[IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\))、[TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) オブジェクトなど) に対しては、ビューにどの Outlook アイテムを表示するかを決定する別のメソッドを使用します。 たとえば、**BusinessCardView** オブジェクトで表示するフィールドは、表示する各 Outlook アイテムに関連付けられた電子名刺 (EBC) のレイアウトによって決定されます。

ビューの **ViewFields** コレクションを取得するには、関連する **View** オブジェクト (たとえば、 **CardView** オブジェクトや **TableView** オブジェクト) の **ViewFields** プロパティを使用します。 **ViewFields** コレクションの **Add** メソッドを使用して、ビューに表示する Outlook のアイテム プロパティを表す [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) オブジェクトを作成します。 **ViewField** オブジェクトは、ビューに表示する Outlook のアイテム プロパティを表すだけでなく、そのプロパティをどのような値として表示するかも記述します。ビューの個々の列のプロパティの表示方法は、 [ViewField](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) オブジェクトの **ColumnFormat** プロパティで変更できます。

次のコード例の ModifyMeetingRequestsView は、ユーザーの受信トレイから "Meeting Requests" (会議出席依頼) ビューと区分されるすべてのビューを表す **TableView** オブジェクトを取得します。次に、**Add** メソッドを使用して、"Start" フィールドと "End" フィールドを、**TableView** オブジェクトに対応する **ViewFields** オブジェクトに追加します。さらに、"From" フィールドのラベルを "Organized By" (開催者) に変更します。その後、ModifyMeetingRequestsView は、変更された **TableView** オブジェクトを保存します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [ビュー](views.md)

