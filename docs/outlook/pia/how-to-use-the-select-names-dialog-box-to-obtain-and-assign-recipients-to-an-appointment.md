---
title: '[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる'
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 57a7c99efa2bd82e1bc3d3f0855a90b62109719c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407003"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a>[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる

この例では、**[名前の選択]** ダイアログ ボックスを使用して、予定アイテムに対する受信者を取得して割り当てる方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[ **名前の選択**] ダイアログ ボックスを表示するには、[SelectNamesDialog](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) オブジェクトの [Display()](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) メソッドを呼び出します。[ **名前の選択**] ダイアログ ボックスをユーザーに対して表示した後、ユーザーが [ **OK**] をクリックするまで、またはダイアログ ボックスを閉じるまで、コードの実行は停止します。ダイアログ ボックスに初期値として表示する受信者を設定したり、ダイアログ ボックスで選択された受信者を取得したりするには、 [SelectNamesDialog](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) オブジェクトの **Recipients** プロパティを使用します。このプロパティは、 [SelectNamesDialog](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) と関連付けられた **Recipients** コレクションを返します。 [SelectNamesDialog](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) の **Recipients** コレクションに **Recipient** オブジェクトを追加するには、コレクションの [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) メソッドを使用し、 [Recipient](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) オブジェクトの **Type** プロパティを指定します。

次のコード例の DemoSelectNamesDialogRecipients では、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成し、いくつかのプロパティを設定します。 その後、 **SelectNamesDialog** を作成し、 [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) メソッドを使用して、[ **名前の選択**] ダイアログ ボックスの会議表示モードを設定します。 この例では、 **Resource** 受信者セレクターに "Conf Room 36/2739" という文字列を設定します。 ダイアログ ボックスをユーザーに表示した後、コードでは **SelectNamesDialog** のこのインスタンスと関連付けられている **Recipients** コレクションを列挙し、これらの受信者を作成された予定に追加します。 最後に、会議出席依頼をユーザーに表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [受信者](recipients.md)

