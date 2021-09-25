---
title: ADO for Windows Foundation クラス (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0be678323e24179c0362f119ecc4dc11bb85b0ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559221"
---
# <a name="adowfc"></a>ADO/WFC


**適用先:** Access 2013、Office 2013

Windows Foundation Classes (ADO/WFC) 用の ADO は、ADO のイベント モデルを基に構築されており、簡素化されたアプリケーション プログラミング インターフェイスを提供します。通常、ADO/WFC は、ADO イベントを取得してイベント パラメーターを単一のイベント クラスに統合してから、イベント ハンドラーを呼び出します。

**ADO/WFC で ADO イベントを使用するには**

1.  イベントを処理するための独自のイベント ハンドラーを定義します。たとえば、 **ConnectionEvent** ファミリの **ConnectComplete** イベントを処理する場合は、次のようなコードを使用できます。
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  作成したイベント ハンドラーを表すハンドラー オブジェクトを定義します。ハンドラー オブジェクトのデータ型は、 **ConnectionEvent** 型のイベントの場合は **ConnectEventHandler** に、また **RecordsetEvent** 型のイベントの場合は **RecordsetEventHandler** にする必要があります。たとえば、 **ConnectComplete** イベント ハンドラーは次のようにコーディングします。
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    **ConnectionEventHandler** コンストラクターの最初の引数は、2 番目の引数で指定されているイベント ハンドラーを含むクラスへの参照です。 Microsoft Visual J++ コンパイラも、これに相当する次のような構文をサポートしています。
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    **ConnectionEventHandler** コンストラクターの最初の引数は、2 番目の引数で指定されているイベント ハンドラーを含むクラスへの参照です。 Microsoft Visual J++ コンパイラも、これに相当する次のような構文をサポートしています。
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    唯一の引数は、目的のクラス (**this**) と、そのクラス内のメソッド (**onConnectComplete**) への参照です。

3.  Add your event handler to a list of handlers designated to process a particular type of event. addOn EventName (ハンドラー) などの名前を _持つメソッド_ を *使用します*。

4.  ADO/WFC では、すべての ADO のイベント ハンドラーが内部的に実装されています。このため、 **Connection** または **Recordset** の操作によって発生するイベントは、ADO/WFC のイベント ハンドラーによって取得されます。 ADO/WFC のイベント ハンドラーは、ADO の **ConnectionEvent** のパラメーターを ADO/WFC の **ConnectionEvent** クラスのインスタンスとして、また ADO の **RecordsetEvent** のパラメーターを ADO/WFC の **RecordsetEvent** クラスのインスタンスとして渡します。これらの ADO/WFC クラスは、ADO イベントのパラメーターを統合したものです。つまり、各 ADO/WFC クラスには、ADO の **ConnectionEvent** または **RecordsetEvent** の全メソッドの一意のパラメーターごとに 1 つのデータ メンバーが含まれます。

5.  次に、ADO/WFC は、ADO/WFC のイベント オブジェクトを使用して、前の手順で作成したイベント ハンドラーを呼び出します。たとえば、 **onConnectComplete** ハンドラーのシグネチャは次のとおりです。
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    最初の引数は、イベントを送信したオブジェクトの型 ([Connection](connection-object-ado.md) または [Recordset](recordset-object-ado.md))、2 番目の引数は、ADO/WFC のイベント オブジェクト (**ConnectionEvent** または **RecordsetEvent**) です。 このイベント ハンドラーのシグネチャは、ADO イベントよりも単純です。 ただし、イベントに適用されるパラメーター、および応答の方法を理解するには、ADO のイベント モデルを理解しておく必要があります。

6.  作成したイベント ハンドラーから、ADO イベントの ADO/WFC ハンドラーに制御が戻ります。ADO/WFC は、関係する ADO/WFC のイベント データ メンバーを ADO のイベント パラメーターにコピーし、ADO のイベント ハンドラーに制御が戻ります。

7.  When you are finished processing, remove your handler from the list of ADO/WFC event handlers. **removeOn** EventName ( ハンドラー) などの名前を _持つメソッド_ を *使用します*。

