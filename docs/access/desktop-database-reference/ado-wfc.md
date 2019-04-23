---
title: Windows Foundation Classes 用の ado (ado/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281723"
---
# <a name="adowfc"></a><span data-ttu-id="016d2-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="016d2-102">ADO/WFC</span></span>


<span data-ttu-id="016d2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="016d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="016d2-p101">Windows Foundation Classes (ADO/WFC) 用の ADO は、ADO のイベント モデルを基に構築されており、簡素化されたアプリケーション プログラミング インターフェイスを提供します。通常、ADO/WFC は、ADO イベントを取得してイベント パラメーターを単一のイベント クラスに統合してから、イベント ハンドラーを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="016d2-p101">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface. In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="016d2-106">**ADO/WFC で ADO イベントを使用するには**</span><span class="sxs-lookup"><span data-stu-id="016d2-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="016d2-p102">イベントを処理するための独自のイベント ハンドラーを定義します。たとえば、 **ConnectionEvent** ファミリの **ConnectComplete** イベントを処理する場合は、次のようなコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="016d2-p102">Define your own event handler to process an event. For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="016d2-p103">作成したイベント ハンドラーを表すハンドラー オブジェクトを定義します。ハンドラー オブジェクトのデータ型は、 **ConnectionEvent** 型のイベントの場合は **ConnectEventHandler** に、また **RecordsetEvent** 型のイベントの場合は **RecordsetEventHandler** にする必要があります。たとえば、 **ConnectComplete** イベント ハンドラーは次のようにコーディングします。</span><span class="sxs-lookup"><span data-stu-id="016d2-p103">Define a handler object to represent your event handler. The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**. For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="016d2-p104">**ConnectionEventHandler** コンストラクターの最初の引数は、2 番目の引数で指定されているイベント ハンドラーを含むクラスへの参照です。 Microsoft Visual J++ コンパイラも、これに相当する次のような構文をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="016d2-p104">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="016d2-p105">**ConnectionEventHandler** コンストラクターの最初の引数は、2 番目の引数で指定されているイベント ハンドラーを含むクラスへの参照です。 Microsoft Visual J++ コンパイラも、これに相当する次のような構文をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="016d2-p105">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="016d2-116">唯一の引数は、目的のクラス (**this**) と、そのクラス内のメソッド (**onConnectComplete**) への参照です。</span><span class="sxs-lookup"><span data-stu-id="016d2-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="016d2-117">Add your event handler to a list of handlers designated to process a particular type of event.</span><span class="sxs-lookup"><span data-stu-id="016d2-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="016d2-118">メソッドには、\**addOn \* \* \* EventName*(*handler*) などの名前を付けて使用します。</span><span class="sxs-lookup"><span data-stu-id="016d2-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="016d2-p107">ADO/WFC では、すべての ADO のイベント ハンドラーが内部的に実装されています。このため、 **Connection** または **Recordset** の操作によって発生するイベントは、ADO/WFC のイベント ハンドラーによって取得されます。 ADO/WFC のイベント ハンドラーは、ADO の **ConnectionEvent** のパラメーターを ADO/WFC の **ConnectionEvent** クラスのインスタンスとして、また ADO の **RecordsetEvent** のパラメーターを ADO/WFC の **RecordsetEvent** クラスのインスタンスとして渡します。これらの ADO/WFC クラスは、ADO イベントのパラメーターを統合したものです。つまり、各 ADO/WFC クラスには、ADO の **ConnectionEvent** または **RecordsetEvent** の全メソッドの一意のパラメーターごとに 1 つのデータ メンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="016d2-p107">ADO/WFC internally implements all the ADO event handlers. Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler. The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class. These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="016d2-p108">次に、ADO/WFC は、ADO/WFC のイベント オブジェクトを使用して、前の手順で作成したイベント ハンドラーを呼び出します。たとえば、 **onConnectComplete** ハンドラーのシグネチャは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="016d2-p108">ADO/WFC then calls your event handler with the ADO/WFC event object. For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="016d2-125">最初の引数は、イベントを送信したオブジェクトの型 ([Connection](connection-object-ado.md) または [Recordset](recordset-object-ado.md))、2 番目の引数は、ADO/WFC のイベント オブジェクト (**ConnectionEvent** または **RecordsetEvent**) です。</span><span class="sxs-lookup"><span data-stu-id="016d2-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="016d2-126">このイベント ハンドラーのシグネチャは、ADO イベントよりも単純です。</span><span class="sxs-lookup"><span data-stu-id="016d2-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="016d2-127">ただし、イベントに適用されるパラメーター、および応答の方法を理解するには、ADO のイベント モデルを理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="016d2-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="016d2-p110">作成したイベント ハンドラーから、ADO イベントの ADO/WFC ハンドラーに制御が戻ります。ADO/WFC は、関係する ADO/WFC のイベント データ メンバーを ADO のイベント パラメーターにコピーし、ADO のイベント ハンドラーに制御が戻ります。</span><span class="sxs-lookup"><span data-stu-id="016d2-p110">Return from your event handler to the ADO/WFC handler for the ADO event. ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="016d2-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span><span class="sxs-lookup"><span data-stu-id="016d2-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="016d2-131">メソッドには、\**removeon \* \* \* EventName*(*handler*) などの名前を付けて使用します。</span><span class="sxs-lookup"><span data-stu-id="016d2-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

