---
title: フォームサーバーコードの記述
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325796"
---
# <a name="writing-form-server-code"></a>フォームサーバーコードの記述

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーは次のように考えることができます。 
  
- 標準の windows メッセージポンプメカニズムを通じて、インターフェイスを表示し、windows メッセージを処理する Win32 プログラム。
    
- ole にクラスファクトリを登録するオブジェクト。 ole オートメーションメソッドによってアクティブ化されます。
    
- 他の mapi コンポーネントとの相互作用に関する mapi ルールに従う mapi オブジェクト。
    
 コードでは、これら3つの広範な要件を同時に処理する必要があります。 
  
フォームサーバーのクラスファクトリの登録の詳細については、「Windows SDK」の「COM および ActiveX のオブジェクトサービス」セクションを参照してください。 windows メッセージの処理とインターフェイスの表示は、MAPI フォームに関して特別な要件を持たない標準の windows プログラミング手法です。 windows SDK には、windows プログラミングの詳細が含まれています。 このドキュメントには、必要な mapi フォームインターフェイスを実装して、他の mapi コンポーネントと対話するための mapi ルールに従うようにするために必要な情報が含まれています。これは、主に mapi フォームマネージャーおよびメッセージングクライアントアプリケーションです。
  
フォームサーバーの実装時に使用できるすべてのインターフェイスは、OLE 基本クラス[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から直接的または間接的に派生しています。 これは、これらのインターフェイスのすべての実装に、 **QueryInterface**、 **AddRef**、および**Release**の各メソッドを含める必要があることを意味します。 複数の継承を使用して、必要なすべてのインターフェイスを独自の1つの新しいクラスに実装すると、使用するすべてのインターフェイスで必要な**IUnknown**メソッドの1つの実装を共有できるようになるため、多くの作業を節約できます。 詳細については、 [iunknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)、 [iunknown::: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)、および[iunknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを参照してください。 これらの方法では、MAPI フォームサーバーに関して特別な考慮事項はありません。 
  
すべてのフォームサーバーですべての MAPI フォームインターフェイスが必須となるわけではありませんが、特定のインターフェイス内のメソッドは必須です。 つまり、特定のインターフェイスを実装することを選択した場合は、そのインターフェイスのすべてのメソッドを実装する必要があります。 これは、メッセージトランスポートなどの他の MAPI コンポーネントの場合とは異なります。 さいわい、MAPI フォームインターフェイスのメソッドは比較的単純なので、すべてを実装しても、開発者にとって大きな負担になることはありません。
  
MAPI フォームインターフェイスは、フォームサーバーの作成に使用される開発ツールの種類に依存しません。 これにより、さまざまな開発ツールを使用してフォームを作成できるようになります。 唯一の要件は、すべてのフォームサーバーが必要な MAPI フォームインターフェイスをサポートする必要があることです。
  
フォームに関連するすべての MAPI インターフェイスがすべてのフォームサーバーで必要となるわけではありません。 オプションのインターフェイスを使用すると、ほとんどのフォームサーバーで必要とされていない高度なフォーム関数を実装できます。 次の表に、インターフェイス、ユーザーについての説明、およびそれらを実装する必要があるかどうかを示します。
  
|**インターフェイス**|**説明**|**状態**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |クライアントがフォームサーバーをロードし、フォーム動詞を実行し、フォームサーバーをシャットダウンするために使用するプライマリインターフェイス。 これは、フォームオブジェクトが実装するインターフェイスに関して、他の ole コンポーネントに通知するために使用される ole **IUnknown**から派生するインターフェイスでもあります。  <br/> |必須  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |フォームオブジェクトにメッセージを読み込むとき、およびメッセージを保存するときに使用されます。  <br/> |必須  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |フォームオブジェクトで使用され、メッセージングクライアントの状態を追跡し、form オブジェクトがフォルダー内の次または前のメッセージを表示できるかどうかを確認します。  <br/> |省略可能  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |ole クラスファクトリメカニズムに準拠するためにフォームオブジェクトで使用される ole クラスファクトリインターフェイス。  <br/> |必須  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |フォームサーバーが複数の種類のフォームをサポートしている場合に使用します。 この場合、 **imapiformfactory**インターフェイスを使用すると、クライアントアプリケーションは、フォームサーバーでも実装する必要がある、複数の**IClassFactory**インターフェイス (フォームサーバーがサポートするフォームの種類ごとに1つ) にアクセスできます。  <br/> |省略可能  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI フォームサーバーの開発](developing-mapi-form-servers.md)

