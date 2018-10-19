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
# <a name="connecting-to-custom-event-handlers"></a>カスタム イベント ハンドラーに接続する

Outlook では、受信トレイでの新規メール アイテムの受信といったできごとが起きると、イベントを発生させてアドインに通知します。アドインでは、特定のイベントが発生したら特定のアクションを実行するように、Outlook に指定できます。この通知とコールバックのしくみは、.NET Framework のデリゲートによってサポートされます。Outlook のプライマリ相互運用機能アセンブリ (PIA) では、対応するイベントを処理するためにコールバック メソッドを接続できるデリゲートが定義されています。ここでは、コールバック メソッドを定義し、それをイベント ハンドラーとして Outlook オブジェクトに接続する処理について説明します。

## <a name="creating-a-callback-method"></a>コールバック メソッドを作成する

コールバックとは、特定のイベントの発生を処理するために実装されて、通知の送信元によって実行されるメソッドです。Outlook では、アドインはコールバック メソッドを実装して、Outlook で発生するイベントに対応できます。このコールバック メソッドは、そのイベントのデリゲートの署名と一致している必要があります。たとえば、 [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) イベントのイベント ハンドラーを実装するには、次のように対応するデリゲートの署名と一致するコールバック メソッドを宣言する必要があります。

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

コールバック メソッドを定義するときは、**Delegate** キーワードを無視します。それ以外の場合は別のデリゲートが定義されます。次にサンプルのコールバック メソッド **MyItemSendEventHandler** を示します。

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a>コールバック メソッドを接続する

イベントのコールバック メソッドを実装した後、それを Outlook オブジェクトに接続して、そのイベントのイベント ハンドラーとしてそのメソッドを呼び出すことを Outlook に認識させることができます。1 つのイベントを複数のイベント ハンドラーで処理でき、このような場合にイベント ハンドラーにイベント処理を割り当てるデリゲートが役割を果たすことに注意してください。

**Application** オブジェクトの **ItemSend** イベント用のイベント ハンドラーを指定する最後の例では、C\# で **MyItemSendEventHandler** を **Application** オブジェクトに接続するために、デリゲート オブジェクトのインスタンスを作成し、**MyItemSendEventHandler** をデリゲート オブジェクトのコンストラクターに渡してから、+= 演算子を使用してこのデリゲート オブジェクトを **ItemSend** イベントに追加します。

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

Visual Basic では、**AddHandler** ステートメントを使用して **ItemSend** イベントを **MyItemSendEventHandler** イベント ハンドラーと関連付けます。

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a>関連項目

- [Outlook PIA でのイベント](events-in-the-outlook-pia.md)
- [Outlook PIA でのオブジェクト](objects-in-the-outlook-pia.md)

