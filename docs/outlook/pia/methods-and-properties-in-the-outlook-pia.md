---
title: Outlook PIA でのメソッドとプロパティ
TOCTitle: Methods and properties in the Outlook PIA
ms:assetid: ec7742de-ead6-41dd-90a3-1280fdf09d54
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612528(v=office.15)
ms:contentKeyID: 55119780
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b1bee381e6f53b4d8a63e69a920e4f4a6e9e302a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407374"
---
# <a name="methods-and-properties-in-the-outlook-pia"></a>Outlook PIA でのメソッドとプロパティ

ここでは、Outlook プライマリ相互運用機能アセンブリ (PIA) を使用してマネージ コードのオブジェクトのメソッドとプロパティにアクセスする方法を説明します。

## <a name="where-helper-objects-come-from"></a>ヘルパー オブジェクトの由来

Outlook PIA を作成するため、Outlook は .NET Framework のタイプ ライブラリ インポーター (TLBIMP) を使用して、COM タイプ ライブラリでの型定義を共通言語ランタイム (CLR) アセンブリでの同等の定義に変換します。COM では、オブジェクトは実際には以下のもので構成されるコクラスです。

- プライマリ インターフェイス (例: [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)) インターフェイス)。

- イベント インターフェイス (例: [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\)) インターフェイス)。

TLBIMP は、各オブジェクトのプライマリ インターフェイスとイベント インターフェイスをインポートし、複数のインターフェイス、デリゲート、およびクラスを作成します。その中には次のものが含まれます。

- .NET イベント インターフェイス (例: [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\)) インターフェイス)。

- .NET クラス (例: [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\)) クラス)。

- .NET インターフェイス (例: [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) インターフェイス)。

## <a name="what-the-helper-objects-are-for"></a>ヘルパー オブジェクトの対象

**FormRegion** オブジェクトを引き続き例として使用し、次のリストでは前に示した各インターフェイスとクラスに含まれるものを説明します。

- \_FormRegion インターフェイスは FormRegion のすべてのメソッドとプロパティを定義します。 通常、後で説明する場合を除き、このインターフェイスをコードで使用することはありません。

- **FormRegionEvents** インターフェイスは、FormRegion のイベントへのメソッドのマッピングを定義します。 このインターフェイスはコードでは使用しません。

- TLBIMP は、**FormRegionEvents** インターフェイスをさらに処理し、FormRegion のすべてのイベントを定義する、**FormRegionEvents**\_Event インターフェイスを作成します。 通常、後で説明する場合を除き、このインターフェイスをコードで使用することはありません。

- FormRegionClass クラスでは、 FormRegion のすべてのメソッド、プロパティ、およびイベントが定義されています。このクラスにより FormRegion インターフェイスが裏側で関連付けられて、 FormRegion インターフェイスのインスタンスを作成するためのコードを記述できます。ただし、コードでこのインターフェイスを直接使用することはありません。

- FormRegion インターフェイスは、\_FormRegion インターフェイスと **FormRegionEvents**\_Event インターフェイスを継承します。 図 1 は、この継承のリレーションシップを示します。
    
  **図 1. FormRegion インターフェイスは \_FormRegion からメソッドとプロパティを継承し、FormRegionEvents\_Event interface** からイベントを継承する

  ![FormRegion インターフェイスは _FormRegion インターフェイスからメソッドとプロパティを継承し、FormRegionEvents_Event インターフェイスからイベントを継承する](media/pia-form-region-interface.gif)
    
  通常、FormRegion は、マネージ コードで **FormRegion** オブジェクトのオブジェクトとメソッド、プロパティ、およびイベント メンバーへアクセスするために使用されるインターフェイスです。

別の例として **Application** オブジェクトを使用すると、 **Application** オブジェクト、メソッド、プロパティ、およびイベントには、 [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) インターフェイスを介してアクセスします。ただし、以下の 3 つの例外的状況では、別のインターフェイスを使用する必要があるか、または言語によっては別のインターフェイスを使用した方がよい場合があります。

- イベントと同じ名前を共有するメソッドにアクセスするときは、プライマリ インターフェイスにキャストしてメソッドを呼び出すのがよい方法です。 たとえば、**Application** オブジェクトには [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) メソッドと [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)) イベントがあります。 Visual Basic .Net では、アプリケーションのインターフェイス経由で Quit メソッドにアクセスできます。 C\# では、次のコード例のように、Quit メソッドをプライマリ インターフェイスにキャストすることにより、コンパイラの警告を回避できます。
    
   ```csharp
      void DemoApp()
      {
          Outlook.Application myApp = new Outlook.Application();
          // Other application code here
          ((Outlook._Application)myApp).Quit();
      }
   ```

- そのオブジェクトのメソッドと同じ名前を共有するイベントにアクセスするときは、適切なイベント インターフェイスにキャストしてイベントに接続する必要があります。 上記の例と似ていますが、Quit イベントに接続するには [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)) インターフェイスにキャストします。

- 以前のバージョンのイベントで、後のバージョンの Outlook において拡張されているものに接続するときは、前のインターフェイスのバージョンのイベントに接続する必要があります。 たとえば、最新バージョンではなくて Outlook 2002 で実装された **Application** オブジェクト用の Quit イベントのバージョンに接続する場合、ApplicationEvents\_11\_Event インターフェイスで定義された Quit イベントではなく、[ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)) インターフェイスで定義された [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) イベントに接続します。

## <a name="see-also"></a>関連項目

- [Outlook PIA とオブジェクト モデルの関係](relating-the-outlook-pia-with-the-object-model.md)
- [Outlook PIA でのオブジェクト](objects-in-the-outlook-pia.md)
- [Outlook PIA でのイベント](events-in-the-outlook-pia.md)

