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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342253"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a><span data-ttu-id="2d5fd-102">イベント ハンドラーで変数の範囲を適切に設定する</span><span class="sxs-lookup"><span data-stu-id="2d5fd-102">Scoping variables appropriately in event handlers</span></span>

<span data-ttu-id="2d5fd-p101">イベント ハンドラーのプログラミングでよくある誤りは、イベント ハンドラーを接続するオブジェクトが、イベント処理の目的には限定されすぎたスコープで宣言されていることです。オブジェクトの有効期間の範囲には、オブジェクトのイベント ハンドラーとしてコールバック メソッドを接続する関数だけでなく、イベントが実際に処理されるコールバック メソッド自体も含まれる必要があります。そのようにしないと、オブジェクトがスコープの範囲外になり、コールバック メソッドで定義されなくなった場合、コールバック メソッドは呼び出されず、イベントは意図したように処理されません。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-p101">A common mistake in programming event handlers is connecting the event handler to an object that has been declared with a scope too limited for the purpose of handling the event. The object must have a life that spans not just over the function that connects the callback method as an event handler of the object, but also over the callback method itself where the event is actually handled. Otherwise, if the object is out of scope and is no longer defined in the callback method, the callback method is not called and the event is not handled as desired.</span></span>

<span data-ttu-id="2d5fd-106">次の例では、MyNewInspector コールバック メソッドを [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) イベントに接続しようとしています。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-106">The following example attempts to connect the MyNewInspector callback method to the [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) event.</span></span> <span data-ttu-id="2d5fd-107">しかし、このコード サンプルのコールバック メソッドは、 Connect 関数に限定されたスコープを持つ [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) オブジェクトの NewInspector イベントに対してフックされます。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-107">However, the callback method is hooked up in the code sample to the NewInspector event of an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) object that has a scope limited to the Connect function.</span></span> <span data-ttu-id="2d5fd-108">このコールバック メソッドが最終的に呼び出されるときには、Connect 関数は既に終了していて、Inspectors オブジェクトは既にガベージ コレクトされていてるため、MyNewInspector が呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-108">When the callback method is eventually called, the Connect function has already exited, the Inspectors object has already been garbage collected, and so MyNewInspector is never called.</span></span>

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

<span data-ttu-id="2d5fd-p103">この場合の正しい方法は、有効期間が MyNewInspector コールバック メソッドを含む MyClass 全体におよぶ、もっと存続期間の長い変数に、Inspectors オブジェクトを格納することです。次の例では、MyInspectors のスコープは MyClass 全体であり、コールバック メソッドがクラスの有効期間に接続されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-p103">The correct thing to do in this case is to store the Inspectors object in a more permanent variable whose lifetime spans over the entire MyClass, including the MyNewInspector callback method. In the following example, MyInspectors has a scope of the entire MyClass and ensures that the callback method is connected for the lifetime of the class.</span></span>

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

<span data-ttu-id="2d5fd-111">各種の言語でイベント ハンドラーに接続する方法には構文的な違いがあるため、Visual Basic のように親オブジェクトのインスタンスを指定しているイベントを接続し、同時にコールバック メソッドを定義できる言語では、この問題はほとんど発生しません。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-111">By virtue of the syntactic differences in how various languages connect event handlers, this issue is less common in languages such as Visual Basic where you can connect an event specifying an instance of the parent object, and define the callback method at the same time.</span></span> <span data-ttu-id="2d5fd-112">次に示す Visual Basic の例では、Handles キーワードを使用して Region\_Expanded コールバック メソッドを [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) イベントに接続しています。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-112">The following example in Visual Basic uses the Handles keyword to connect the Region\_Expanded callback method to the [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) event.</span></span> <span data-ttu-id="2d5fd-113">親オブジェクトのインスタンス Region には、Region\_Expanded コールバック メソッドが含まれている MyClass を範囲に収めるスコープがあります。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-113">An instance of the parent object, Region, has a scope that spans MyClass including the Region\_Expanded callback method.</span></span>

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

<span data-ttu-id="2d5fd-114">この例では、クラスの有効期間中は Region\_Expanded コールバック メソッドが Expanded イベントに接続されているため、コールバック メソッドは正しく呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-114">In this example, because the Region\_Expanded callback method is connected to the Expanded event for the lifetime of the class, the callback method is called as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d5fd-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d5fd-115">See also</span></span>

- [<span data-ttu-id="2d5fd-116">カスタム イベント ハンドラーに接続する</span><span class="sxs-lookup"><span data-stu-id="2d5fd-116">Connecting to custom event handlers</span></span>](connecting-to-custom-event-handlers.md)

