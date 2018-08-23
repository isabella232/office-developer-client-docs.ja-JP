---
title: MAPI オブジェクトとインターフェイスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4f69985f9cdaaba0681b823e6fe448d009ee9dfa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585711"
---
# <a name="mapi-object-and-interface-overview"></a>MAPI オブジェクトとインターフェイスの概要

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI オブジェクトは、オブジェクト クラスの C++ または C のデータ構造体の 1 つまたは複数の MAPI インターフェイス、または関連する関数のコレクションから継承します。 関連する関数のこれらのコレクションは、C++ 開発者にとって、純粋仮想関数と呼ばれます。 純粋仮想関数では、MAPI には、のみ関数プロトタイプ実装ではなくが用意されています。 クライアント アプリケーション、サービス プロバイダー、または MAPI を提供するこの実装はメッセージング API の関数の説明に準拠しているインターフェイスを継承するオブジェクト クラスを作成して予定です。 MAPI インターフェイスは、継承クラスでのみインスタンス化できます。
  
別の MAPI オブジェクトが多く、最終的には、 [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)インターフェイスから継承されているインターフェイスから継承する各オブジェクトがあります。 **IUnknown**は、OLE コンポーネント オブジェクト モデル (COM) の基本インターフェイスです。 通信と制御のための標準的なメカニズムに MAPI オブジェクトを提供します。 COM オブジェクトの実装がメモリ管理では、パラメーターの管理などの問題を処理する方法を決定し、マルチ スレッドです。 このモデルに準拠する、ことでは、オブジェクトの実装側は、オブジェクトに含まれているインタ フェースが指定されている契約に準拠します。 
  
他で継承されていない直接他の 2 つの基本インターフェイスのいずれかの中に、多数の MAPI インターフェイスが**IUnknown**から直接継承されます: [IMAPIProp: IUnknown](imapipropiunknown.md)のプロパティの管理と[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)フォルダーのとアドレス帳にアクセスします。 独立したスタンドアロン オブジェクトとしての基本インターフェイスを実装しません。常に他のオブジェクトの一部として実装される、派生インターフェイスを実装するオブジェクトです。 
  
1 つまたは複数の MAPI コンポーネントによって実装されている各、MAPI は、多くの種類のオブジェクトを定義します。 クライアントによって実装されたオブジェクトは、MAPI によって、サービス プロバイダー、およびカスタム フォームのコンポーネントに使用されます。 サービス プロバイダーによって実装されたオブジェクトは、MAPI によって、クライアントが通常使用されます。 オブジェクトは、フォーム ライブラリのプロバイダーによって実装されているし、他のフォームのコンポーネントとクライアントによってフォームのサーバーを使用します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MAPI の概念](mapi-concepts.md)

