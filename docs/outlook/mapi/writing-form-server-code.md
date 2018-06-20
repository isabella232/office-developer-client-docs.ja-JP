---
title: フォーム サーバー コードの記述
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 860b0150fd1ec66fa8fee387d8d4a96e8bb79761
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804232"
---
# <a name="writing-form-server-code"></a>フォーム サーバー コードの記述

  
  
**適用されます**: Outlook 
  
フォーム サーバーとして、次の考えることができます。 
  
- インタ フェースを表示し、標準の Windows メッセージ ポンプの機構を使用して windows メッセージを処理する Win32 プログラムです。
    
- クラス ファクトリを OLE に登録し、OLE オートメーションのメソッドがアクティブにするオブジェクト。
    
- 他の MAPI コンポーネントとの相互作用の MAPI の規則に従っている MAPI オブジェクトを返します。
    
 コード内に、これらの広範な要件の 3 つすべてを同時に処理します。 
  
詳細については、フォーム サーバーのクラス ファクトリの登録に関する Windows SDK の COM および ActiveX オブジェクト サービスのセクションを参照してください。 Windows メッセージを処理して、インターフェイスを表示するは、MAPI フォームに関して特別な要件がない標準的な Windows プログラミング手法です。 もう一度、Windows SDK では、Windows プログラミングに関する詳細情報があります。 このドキュメントには、必須および省略可能な MAPI フォームのインタ フェースを実装して、他の MAPI コンポーネントとの相互作用の MAPI 規則に従っているようにするために知っておくべき-MAPI では主にマネージャーとメッセージング クライアント アプリケーションを形成します。
  
すべてのフォームのサーバーを実装する際に使用できるインターフェイスは、派生-直接または間接的に、OLE からは、基本クラスの[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)。 これは、すべてのこれらのインターフェイスの実装は、 **QueryInterface**、 **AddRef**、および**Release**メソッドを持っている必要があることを意味します。 使用するすべてのインタ フェースが必要な**IUnknown**のメソッドの 1 つの実装を共有できるように、独自の新しいクラスの 1 つですべての必要なインターフェイスを実装するために複数の継承を使用する場合、多くの作業が保存できます。 詳細については、 [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)、 [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)、および[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを参照してください。 これらのメソッドには、MAPI フォームのサーバーに対する特別な考慮事項はありません。 
  
MAPI フォームのインタ フェースのすべてのフォームのすべてのサーバーでは必須ですが、任意の指定されたインターフェイスのメソッドは必須です。 特定のインタ フェースを実装する場合は、必要がありますを実装するすべてのメソッドのインターフェイスで。 これは、メッセージ トランスポートなどの他の MAPI コンポーネントの場合とは異なります。 幸いなことに、MAPI フォームのインタ フェース内のメソッドは比較的単純ですが、それらのすべてを実装することも、大きな負担の開発者のためです。
  
MAPI フォームのインタ フェースは、フォームのサーバーを作成するために使用する開発ツールの種類に依存しません。 これにより、さまざまな開発ツールを使用して作成するフォームです。 唯一の要件は、フォームのすべてのサーバーが必要な MAPI フォームのインタ フェースをサポートする必要があります。
  
フォームのすべてのサーバーですべてのフォームに関連する MAPI インターフェイスが必要です。 省略可能なインターフェイスを使用すると、フォームのほとんどのサーバーを必要としませんが一部の高度なフォーム機能を実装できます。 次の表は、インタ フェース、それらは何をしてかどうか実装する必要があります。
  
|**インターフェイス**|**説明**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm: IUnknown](imapiformiunknown.md) <br/> |クライアント フォームのサーバーの読み込みに使用する主要なインターフェイスは、フォームの動詞を実行し、フォームのサーバーをシャット ダウンします。 これは、フォーム オブジェクトが実装するインターフェイスについては、他の OLE コンポーネントを通知するために使用される OLE **IUnknown**から派生するインターフェイス。  <br/> |必須  <br/> |
|[IPersistMessage: IUnknown](ipersistmessageiunknown.md) <br/> |フォーム オブジェクトからのメッセージの保存との間にメッセージを読み込むときに使用します。  <br/> |必須  <br/> |
|[IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) <br/> |メッセージング クライアントのステータスを追跡して、フォーム オブジェクトがフォルダー内の次または前のメッセージを表示できるかどうかを確認するのには、フォーム オブジェクトによって使用されます。  <br/> |省略可能  <br/> |
|[IClassFactory](http://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |OLE クラス ファクトリのメカニズムに準拠するために、フォーム オブジェクトによって使用される OLE クラス ファクトリ インターフェイスです。  <br/> |必須  <br/> |
|[IMAPIFormFactory: IUnknown](imapiformfactoryiunknown.md) <br/> |フォーム サーバーが複数の種類のフォームをサポートしている場合に使用されます。 この例では、 **IMAPIFormFactory**インターフェイスを使用 (フォーム サーバーがサポートするフォームの種類ごとに 1 つ) 複数の**IClassFactory**インターフェイスにアクセスするクライアント アプリケーション、フォームのサーバーを実装する必要がありますもことです。  <br/> |省略可能  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI フォームのサーバーの開発](developing-mapi-form-servers.md)

