---
title: フォーム サーバー コードの作成
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325796"
---
# <a name="writing-form-server-code"></a>フォーム サーバー コードの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム サーバーは、次のように考えて使用できます。 
  
- 標準の Windows メッセージ ポンプ メカニズムを使用して、インターフェイスを表示し、Windows メッセージを処理する Win32 プログラム。
    
- クラス ファクトリを OLE に登録し、OLE オートメーション メソッドによってアクティブ化されるオブジェクト。
    
- 他の MAPI コンポーネントとの対話のための MAPI ルールに従う MAPI オブジェクト。
    
 コードでは、これらの 3 つの広範な要件を同時に処理する必要があります。 
  
フォーム サーバーのクラス ファクトリActiveX詳細については、Windows SDK の COM およびオブジェクト サービス のセクションを参照してください。 Windows メッセージの処理とインターフェイスの表示は、MAPI フォームに関する特別な要件を持たない標準的な Windows プログラミング手法です。 繰り返しますが、Windows SDK には Windows プログラミングに関する詳細があります。 このドキュメントには、必要な MAPI フォーム インターフェイスとオプションの MAPI フォーム インターフェイスを実装するために知る必要がある情報が含まれているので、MAPI の他のコンポーネント (主に MAPI フォーム マネージャーとメッセージング クライアント アプリケーション) とのやり取りのための MAPI ルールに従います。
  
フォーム サーバーを実装するときに使用できるすべてのインターフェイスは、OLE 基本クラス [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から直接または間接的に派生します。 つまり、これらのインターフェイスのすべての実装には **、QueryInterface** メソッド **、AddRef** メソッド、および **Release** メソッドが必要になります。 複数の継承を使用して、必要なすべてのインターフェイスを独自の 1 つの新しいクラスに実装する場合は、多くの作業を節約できます。そのため、使用するインターフェイスはすべて、必要な **IUnknown** メソッドの 1 つの実装を共有できます。 詳細については[、「IUnknown::AddRef」、IUnknown::QueryInterface、](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)[および IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを参照してください。 [](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) これらのメソッドの MAPI フォーム サーバーに関する特別な考慮事項はありません。 
  
すべての MAPI フォーム インターフェイスがすべてのフォーム サーバーで必須ではありませんが、特定のインターフェイスのメソッドは必須です。 つまり、特定のインターフェイスを実装する場合は、インターフェイス内のすべてのメソッドを実装する必要があります。 これは、メッセージ トランスポートなど、他の MAPI コンポーネントの状況とは異なります。 幸いなことに、MAPI フォーム インターフェイスのメソッドは比較的簡単なので、すべてのメソッドを実装しても、開発者に大きな負担はかからされません。
  
MAPI フォーム インターフェイスは、フォーム サーバーの作成に使用される開発ツールの種類に依存しません。 これにより、さまざまな開発ツールを使用してフォームを作成できます。 唯一の要件は、すべてのフォーム サーバーが必要な MAPI フォーム インターフェイスをサポートする必要がある場合です。
  
フォームに関連付ける MAPI インターフェイスの一部が、すべてのフォーム サーバーで必要になるとは言えありません。 オプションのインターフェイスを使用すると、ほとんどのフォーム サーバーでは必要ない高度なフォーム関数を実装できます。 次の表に、インターフェイス、インターフェイスの詳細、およびインターフェイスを実装する必要があるかどうかを示します。
  
|**インターフェイス**|**説明**|**状態**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |クライアントがフォーム サーバーの読み込み、フォーム動詞の実行、フォーム サーバーのシャットダウンに使用するプライマリ インターフェイス。 これは、フォーム オブジェクトが実装するインターフェイスに関して他の OLE コンポーネントに通知するために使用される OLE **IUnknown** から派生したインターフェイスです。  <br/> |必須  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |フォーム オブジェクトにメッセージを読み込み、メッセージを保存するときに使用します。  <br/> |必須  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |フォーム オブジェクトを使用して、メッセージング クライアントの状態を追跡し、フォーム オブジェクトがフォルダー内の次のメッセージまたは前のメッセージを表示できるかどうかを確認します。  <br/> |省略可能  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |OLE クラスファクトリ メカニズムに準拠するためにフォーム オブジェクトで使用される OLE クラスファクトリ インターフェイス。  <br/> |必須  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |フォーム サーバーが複数の種類のフォームをサポートしている場合に使用します。 この場合 **、IMAPIFormFactory** インターフェイスを使用すると、クライアント アプリケーションはフォーム サーバーも実装する必要がある複数 **の IClassFactory** インターフェイス (フォーム サーバーがサポートするフォームの種類ごとに 1 つ) にアクセスできます。  <br/> |省略可能  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

