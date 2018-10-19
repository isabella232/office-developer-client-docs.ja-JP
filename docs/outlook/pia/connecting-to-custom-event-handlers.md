---
title: カスタム イベント ハンドラーに接続する
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 31e9a5453bbfbd4a51132fa6af71b86889b4b32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406107"
---
# <a name="connecting-to-custom-event-handlers"></a><span data-ttu-id="cf990-102">カスタム イベント ハンドラーに接続する</span><span class="sxs-lookup"><span data-stu-id="cf990-102">Connecting to Custom Event Handlers</span></span>

<span data-ttu-id="cf990-p101">Outlook では、受信トレイでの新規メール アイテムの受信といったできごとが起きると、イベントを発生させてアドインに通知します。アドインでは、特定のイベントが発生したら特定のアクションを実行するように、Outlook に指定できます。この通知とコールバックのしくみは、.NET Framework のデリゲートによってサポートされます。Outlook のプライマリ相互運用機能アセンブリ (PIA) では、対応するイベントを処理するためにコールバック メソッドを接続できるデリゲートが定義されています。ここでは、コールバック メソッドを定義し、それをイベント ハンドラーとして Outlook オブジェクトに接続する処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf990-p101">Outlook raises events to notify add-ins about something happening, such as the Inbox receiving a new mail item. Add-ins can specify to Outlook that upon the occurrence of a specific event, certain actions should take place. This alert and callback mechanism is supported by delegates of the .NET Framework. The Outlook Primary Interop Assembly (PIA) defines delegates to which you can connect callback methods to handle corresponding events. This topic describes this process of defining a callback method and connecting it as an event handler to the Outlook object.</span></span>

## <a name="creating-a-callback-method"></a><span data-ttu-id="cf990-108">コールバック メソッドを作成する</span><span class="sxs-lookup"><span data-stu-id="cf990-108">Creating a Callback Method</span></span>

<span data-ttu-id="cf990-p102">コールバックとは、特定のイベントの発生を処理するために実装されて、通知の送信元によって実行されるメソッドです。Outlook では、アドインはコールバック メソッドを実装して、Outlook で発生するイベントに対応できます。このコールバック メソッドは、そのイベントのデリゲートの署名と一致している必要があります。たとえば、 [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) イベントのイベント ハンドラーを実装するには、次のように対応するデリゲートの署名と一致するコールバック メソッドを宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf990-p102">A callback is a method that is implemented to handle the occurrence of a specific event and is executed by a notification source. In Outlook, add-ins can implement callback methods to respond to certain events raised by Outlook. This callback method must match the signature of the delegate of that event. For example, to implement an event handler for the [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) event, you must declare the callback method that matches the signature of the corresponding delegate:</span></span>

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

<span data-ttu-id="cf990-p103">コールバック メソッドを定義するときは、**Delegate** キーワードを無視します。それ以外の場合は別のデリゲートが定義されます。次にサンプルのコールバック メソッド **MyItemSendEventHandler** を示します。</span><span class="sxs-lookup"><span data-stu-id="cf990-p103">When defining the callback method, ignore the **Delegate** keyword which otherwise would define another delegate. A sample callback method, **MyItemSendEventHandler**, is shown below:</span></span>

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a><span data-ttu-id="cf990-115">コールバック メソッドを接続する</span><span class="sxs-lookup"><span data-stu-id="cf990-115">Connecting a Callback Method</span></span>

<span data-ttu-id="cf990-p104">イベントのコールバック メソッドを実装した後、それを Outlook オブジェクトに接続して、そのイベントのイベント ハンドラーとしてそのメソッドを呼び出すことを Outlook に認識させることができます。1 つのイベントを複数のイベント ハンドラーで処理でき、このような場合にイベント ハンドラーにイベント処理を割り当てるデリゲートが役割を果たすことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cf990-p104">After implementing a callback method for an event, you can connect it to the Outlook object so that Outlook knows to call the method as an event handler of that event. Note that an event can be handled by more than one event handler, and this is where delegates that assign event handling to event handlers come into play.</span></span>

<span data-ttu-id="cf990-118">**Application** オブジェクトの **ItemSend** イベント用のイベント ハンドラーを指定する最後の例では、C\# で **MyItemSendEventHandler** を **Application** オブジェクトに接続するために、デリゲート オブジェクトのインスタンスを作成し、**MyItemSendEventHandler** をデリゲート オブジェクトのコンストラクターに渡してから、+= 演算子を使用してこのデリゲート オブジェクトを **ItemSend** イベントに追加します。</span><span class="sxs-lookup"><span data-stu-id="cf990-118">Continuing with the last example of specifying a event handler for the **ItemSend** event of the **Application** object, to connect **MyItemSendEventHandler** to the **Application** object in C#, create an instance of the delegate object, pass **MyItemSendEventHandler** to the constructor of the delegate object, and then add this delegate object to the **ItemSend** event using the += operator:</span></span>

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

<span data-ttu-id="cf990-119">Visual Basic では、**AddHandler** ステートメントを使用して **ItemSend** イベントを **MyItemSendEventHandler** イベント ハンドラーと関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cf990-119">In Visual Basic, you use the **AddHandler** statement to associate the **ItemSend** event with the **MyItemSendEventHandler** event handler:</span></span>

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a><span data-ttu-id="cf990-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf990-120">See also</span></span>

- [<span data-ttu-id="cf990-121">Outlook PIA でのイベント</span><span class="sxs-lookup"><span data-stu-id="cf990-121">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)
- [<span data-ttu-id="cf990-122">Outlook PIA でのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="cf990-122">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)

