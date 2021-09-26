---
title: Outlook PIA でのイベント
TOCTitle: Events in the Outlook PIA
ms:assetid: 1f9eafb3-6645-4e27-81fa-5d73bf94ae40
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb644571(v=office.15)
ms:contentKeyID: 55119782
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8124c34e979d76cca6d2e5ab0c1e9896a3c8ecc0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583206"
---
# <a name="events-in-the-outlook-pia"></a>Outlook PIA でのイベント

Outlook プライマリ相互運用機能アセンブリ (PIA) をブラウズすると、Outlook オブジェクト モデルで見慣れたオブジェクト名やイベント名に基づく名前のインターフェイスおよびイベント デリゲートが多数あることがわかります。COM タイプ ライブラリのイベントとは異なり、Outlook PIA のイベントは同じオブジェクトのメソッドやプロパティと同じインターフェイスでは定義されません。Outlook PIA のイベントをサポートするには、イベント関連のインターフェイス、デリゲート、およびシンク ヘルパー クラスをインポートするか作成します。このトピックでは、これらのイベント関連のインターフェイス、デリゲート、およびシンク ヘルパー クラスについて説明します。

## <a name="where-do-the-event-interfaces-delegates-and-sink-helper-classes-come-from"></a>イベントのインターフェイス、デリゲート、シンク ヘルパー クラスの取得

Outlook は、Outlook PIA を作成するために .NET Framework のタイプ ライブラリ インポーター (TLBIMP) を使用して COM タイプ ライブラリのタイプの定義を共通言語ランタイム (CLR) アセンブリの同等の定義に変換します。TLBIMP は、オブジェクトごとに次の 2 種類のインターフェイスをインポートします。

  - プライマリ インターフェイス (例: [\_Application](https://msdn.microsoft.com/library/bb611255\(v=office.15\)) インターフェイス)

  - イベント インターフェイス (例: [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\)) インターフェイス)

TLBIMP は、インポートしたインターフェイスを処理し, .NET インターフェイス (たとえば、[Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) インターフェイス) などの、いくつかのインターフェイス、デリゲート、およびクラスを作成します。オブジェクトにイベントがある場合は、次のものが作成されます。

  - .NET イベント インターフェイス (例: [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)) インターフェイス)

  - 各イベントのデリゲート (たとえば、 [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\)) デリゲート)

  - シンク ヘルパー クラス (たとえば、 [ApplicationEvents\_11\_SinkHelper](https://msdn.microsoft.com/library/bb609842\(v=office.15\)) クラス)

### <a name="multiple-versions-of-events"></a>複数のバージョンのイベント

Outlook の複数のバージョンにわたって存在してきたオブジェクトの中には、バージョンによってイベントの実装が異なるものや、新しいバージョンがリリースされたときに追加的なイベントが増やされたものがあります。Outlook では、複数のバージョンの間で変化するイベントに対応するために、その名前にバージョン番号を付加してイベント関連のインターフェイス、デリゲート、およびクラスを識別しています。以下に例を示します。

  - **Application** オブジェクトに関してインポートされるイベント インターフェイス
    
      - Outlook 98 および Outlook 2000 用の最初のバージョン: [ApplicationEvents](https://msdn.microsoft.com/library/bb644093\(v=office.15\)) インターフェイス
    
      - Outlook 2002 用のバージョン: [ApplicationEvents\_10](https://msdn.microsoft.com/library/bb647702\(v=office.15\)) インターフェイス
    
      - Outlook 2003 以降のリリース用のバージョン: [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\)) インターフェイス

  - **Application** オブジェクトで TLBIMP によって作成される .NET イベント インターフェイスに含まれるもの:
    
      - Outlook 98 および Outlook 2000 用の最初のバージョン: [ApplicationEvents\_Event](https://msdn.microsoft.com/library/bb609380\(v=office.15\)) インターフェイス
    
      - Outlook 2002 用のバージョン: [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)) インターフェイス
    
      - Outlook 2003 以降のリリース用のバージョン: [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)) インターフェイス

  - **Application** オブジェクトの各バージョンでイベントごとに TLBIMP が作成するデリゲート (例: ItemSend イベントの各バージョンのデリゲート)
    
      - Outlook 98 および Outlook 2000 用の最初のバージョン: [ApplicationEvents\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb622515\(v=office.15\)) デリゲート
    
      - Outlook 2002 用のバージョン: [ApplicationEvents\_10\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb646436\(v=office.15\)) デリゲート
    
      - Outlook 2003 以降のリリース用のバージョン: [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\)) デリゲート

新しいバージョンで追加されたイベントは、それ以前のバージョンではイベント インターフェイスに含まれず、対応するデリゲートもありません。たとえば、[AttachmentSelectionChange](https://msdn.microsoft.com/library/ff184926\(v=office.15\)) イベントは Outlook 2010 で [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトに追加されたので、 Explorer オブジェクトの以前のイベント インターフェイスには含まれていません。

  - ExplorerEvents インターフェイス

  - ExplorerEvents\_ イベント インターフェイス

その一方、このイベントは最新の .NET イベント インターフェイスである ExplorerEvents\_10\_Event にあり、また、それに対応する Outlook 2010 用のデリゲートは [ExplorerEvents\_10\_AttachmentSelectionChangeEventHandler](https://msdn.microsoft.com/library/ff185177\(v=office.15\)) にあります。

## <a name="what-the-event-interfaces-delegates-and-sink-helper-classes-are-for"></a>イベント インターフェイス、デリゲート、シンク ヘルパー クラスの目的

このセクションでは、**Application** オブジェクトを例として使用し、上記の各インターフェイスおよびクラスの内容を説明します。

  - プライマリ インターフェイスである \_Application は、Application のすべてのメソッドおよびプロパティを定義します。 通常、後で説明する場合を除き、このインターフェイスをコードで使用することはありません。

  - TLBIMP がインポートするイベント インターフェイス (例: ApplicationEvents\_11 や ApplicationEvents\_10 など) では、Outlook の対応するバージョンの Application のイベントに対するメソッド マッピングが定義されます。 このインターフェイスはコードでは使用しません。

  - TLBIMP によって作成されるイベント インターフェイス (例: ApplicationEvents\_11\_Event や ApplicationEvents\_10\_Event など) では、Outlook の対応するバージョンの Application のすべてのイベントが定義されます。 特定のバージョンのイベントのイベント ハンドラーを設計するときは、イベント ハンドラーをメソッドとして実装し、そのメソッドを, .NET イベント インターフェイスの対応するバージョンで定義されているイベントに接続します。 通常、後で説明する場合を除き、このイベント インターフェイスをコードで参照することはありません。

  - .NET インターフェイスである Application は、\_Application インターフェイスおよび ApplicationEvents\_11\_Event インターフェイスを継承します。 通常、これはマネージ コードでオブジェクト、メソッド、プロパティ、および **Application** オブジェクトの最新のイベント メンバーにアクセスするとき使用するインターフェイスです。 ただし、次の 2 つのケースでは, .NET インターフェイスではなく、別のインターフェイスを使用してイベントに接続します。
    
      - アクセスするイベントの名前が、そのオブジェクトのメソッドと同じときは、適切なイベント インターフェイスにキャストしてイベントに接続します。 たとえば、[Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)) イベントに接続するには ApplicationEvents\_11\_Event インターフェイスにキャストします。
    
      - 以降の新しいバージョンの Outlook で拡張されたイベントの以前のバージョンに接続するときは、以前のインターフェイスのイベントのバージョンに接続します。 たとえば、最新バージョンではなくて Outlook 2002 で実装された **Application** オブジェクト用の Quit イベントのバージョンに接続する場合、ApplicationEvents\_11\_Event インターフェイスで定義された Quit イベントではなく、ApplicationEvents\_10\_Event インターフェイスで定義された [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) イベントに接続します。

  - デリゲートは、特定のバージョンの Outlook で特定のイベントのカスタム イベント ハンドラーを作成するためのフレームワークを提供します。 たとえば、Outlook アイテムで、送信直前に行う件名の有無の確認を追加する場合は、デリゲートと同じ署名を持つコールバック メソッド ApplicationEvents\_11\_ItemSendEventHandler で確認を実装します。 次に、コールバック メソッドを、ApplicationEvents\_11\_Event インターフェイスで定義された ItemSend イベント用のイベント ハンドラーとして接続します。 オブジェクトのイベント ハンドラーとしてのコールバック メソッドの接続に関する詳細については、「[カスタム イベント ハンドラーに接続する](connecting-to-custom-event-handlers.md)」を参照してください。

  - TLBIMP によって作成されるシンク ヘルパー クラス (例: ApplicationEvents\_11\_SinkHelper や [ApplicationEvents\_10\_SinkHelper](https://msdn.microsoft.com/library/bb644070\(v=office.15\)) など) は、Outlook の対応するバージョンの Application イベント用のイベント ヘルパー オブジェクトです。 これらのクラスはコードで使わないでください。

## <a name="see-also"></a>関連項目

- [Outlook PIA とオブジェクト モデルの関係](relating-the-outlook-pia-with-the-object-model.md)
- [Outlook PIA でのオブジェクト](objects-in-the-outlook-pia.md)
- [Outlook PIA でのメソッドとプロパティ](methods-and-properties-in-the-outlook-pia.md)
- [Outlook PIA を使用してマネージ Outlook アドインを開発する](developing-managed-outlook-add-ins-using-the-outlook-pia.md)

