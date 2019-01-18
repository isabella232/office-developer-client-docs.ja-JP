---
title: イベント ハンドラーで変数の範囲を適切に設定する
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8a1a418a315167cc96be5b9b5f65a0f4cd9ce44
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708138"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a>イベント ハンドラーで変数の範囲を適切に設定する

イベント ハンドラーのプログラミングでよくある誤りは、イベント ハンドラーを接続するオブジェクトが、イベント処理の目的には限定されすぎたスコープで宣言されていることです。オブジェクトの有効期間の範囲には、オブジェクトのイベント ハンドラーとしてコールバック メソッドを接続する関数だけでなく、イベントが実際に処理されるコールバック メソッド自体も含まれる必要があります。そのようにしないと、オブジェクトがスコープの範囲外になり、コールバック メソッドで定義されなくなった場合、コールバック メソッドは呼び出されず、イベントは意図したように処理されません。

次の例では、MyNewInspector コールバック メソッドを [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) イベントに接続しようとしています。 しかし、このコード サンプルのコールバック メソッドは、 Connect 関数に限定されたスコープを持つ [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) オブジェクトの NewInspector イベントに対してフックされます。 このコールバック メソッドが最終的に呼び出されるときには、Connect 関数は既に終了していて、Inspectors オブジェクトは既にガベージ コレクトされていてるため、MyNewInspector が呼び出されることはありません。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyApp.Inspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

この場合の正しい方法は、有効期間が MyNewInspector コールバック メソッドを含む MyClass 全体におよぶ、もっと存続期間の長い変数に、Inspectors オブジェクトを格納することです。次の例では、MyInspectors のスコープは MyClass 全体であり、コールバック メソッドがクラスの有効期間に接続されることが保証されます。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;
    private Outlook.Inspectors MyInspectors;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyInspectors = MyApp.Inspectors;
        MyInspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

各種の言語でイベント ハンドラーに接続する方法には構文的な違いがあるため、Visual Basic のように親オブジェクトのインスタンスを指定しているイベントを接続し、同時にコールバック メソッドを定義できる言語では、この問題はほとんど発生しません。 次に示す Visual Basic の例では、Handles キーワードを使用して Region\_Expanded コールバック メソッドを [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) イベントに接続しています。 親オブジェクトのインスタンス Region には、Region\_Expanded コールバック メソッドが含まれている MyClass を範囲に収めるスコープがあります。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Public Class MyClass
    ' The Region object has a lifetime spanning the class 
    ' including the callback method Region_Expanded
    Private WithEvents Region As Outlook.FormRegion
    ...
    Private Sub Region_Expanded() Handles Region.Expanded
        MsgBox("My EventHandler caught an Expanded event.")
    End Sub
End Class
```

この例では、クラスの有効期間中は Region\_Expanded コールバック メソッドが Expanded イベントに接続されているため、コールバック メソッドは正しく呼び出されます。

## <a name="see-also"></a>関連項目

- [カスタム イベント ハンドラーに接続する](connecting-to-custom-event-handlers.md)

