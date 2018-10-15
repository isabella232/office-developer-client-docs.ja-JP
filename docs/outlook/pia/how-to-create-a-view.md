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
# <a name="create-a-view"></a>ビューを作成する

この例では、[Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) コレクションの [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) メソッッドを使用して [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトのビューを作成します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


Outlook エクスプローラー ウィンドウのビュー ウィンドウ内で種類の異なるデータの並べ替え、グループ化、および表示ができるカスタマイズ可能なビューを作成できます。組み込みビューをプログラムによってカスタマイズすることもできます。次の表は、Outlook のビューを表現するオブジェクトの一覧です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクト名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></p></td>
<td><p>データは一連の電子名刺画像として表示されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></p></td>
<td><p>データが予定表の形式で表示されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></p></td>
<td><p>データが一連のカードで表示されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></p></td>
<td><p>データが Windows のフォルダー アイコンまたはエクスプローラー アイコンとして表示されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></p></td>
<td><p>データが単純なフィールド ベースの表で表示されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></p></td>
<td><p>データがカスタマイズ可能な直線状のタイムラインで表示されます。</p></td>
</tr>
</tbody>
</table>


[View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) オブジェクトを使用してすべてのビューに共通するプロパティとメソッドにアクセスすることができます。 ただし、すべてのビューに共通ではない一部のプロパティにアクセスするにするには、**View** オブジェクトを、アクセスするプロパティが属する派生 **View** オブジェクトにキャストする必要があります。 たとえば、**Cardview** オブジェクトの [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) プロパティにアクセスするには、**View** オブジェクトを **Cardview** オブジェクトにキャストします。 特定の **View** オブジェクトでどの種類のビューが表示されるかを確認するには [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) プロパティを使用します。

新しいビューを作成するには、 **Folder** オブジェクトに対する **Views** コレクションの **Add** メソッドを使用します。 次に、作成時またはビューの作成後任意の時にビューの可視性を設定します。 ビューの可視性を作成時に設定するには、**Add** メソッドで *SaveOption* パラメーターの [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) 定数を指定します。 ビューの可視性をビューの作成後の任意の時点で設定するには、 **View** オブジェクトの [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) プロパティに対して **OlViewSaveOption** 定数を指定します。 

新しいビューを追加すると、 [Views](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) コレクションの **ViewAdd** イベントが発生します。 ビューが作成されたら、 **View** オブジェクトを派生オブジェクトの 1 つにキャストしてから必要な変更を行うことにより、そのビューをプログラムでカスタマイズします。 派生 **View** オブジェクトまたは **View** オブジェクトの **Save** メソッドを使用してビューへの変更を保存します。 最後に、派生 **View** オブジェクトまたは **View** オブジェクトの **Apply** メソッドを使用してビューを現在の [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトに適用します。 これにより、**Explorer** オブジェクトの [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) イベントが発生します。

次のコード例では、**View** オブジェクトを **TableView** オブジェクトにキャストすることにより、CreateMeetingRequestsView が “Meeting Requests” という名前の新しいビューをユーザーの受信トレイに追加します。 次に、CreateMeetingRequestsView は、 *Name* パラメーターは “Meeting Requests”、また *ViewType* パラメーターは **olTableView** という設定で **View** オブジェクトの **Add** メソッドを呼び出します。 **TableView** オブジェクトの [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) プロパティは、アイテムのメッセージ クラスに “IPM.Schedule” が含まれているアイテムが存在する場合に限りビューを表示させる DAV Searching and Locating (DASL) 文字列に設定されます。 新しいビューが保存され、適用されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [ビュー](views.md)

